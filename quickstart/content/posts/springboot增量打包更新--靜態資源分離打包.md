
+++
title = 'springboot增量打包更新--靜態資源分離打包'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more-->springboot部署打包爲jar，一般都是全量打包，jar包的大小通常都是超過100M的，並且在進行一般的頁面html微調、js修改、img替換、css樣式修改時也需要重新打包進行部署；每次微小的調整都需要重新打包就太煩了，一般在項目開發穩定以後項目中引用的jar就不再改變
爲了方便進行靜態資源管理及增量部署，對項目引用jar包以及靜態資源分離打包，提高打包的效率及部分前端微調項修改後及時進行無重啓更新；
具體步驟如下：
1、初次打包進行全量打包，對打包的jar進行解壓，解壓後的文件如下圖展示：

2、分離引用的jar包：進入BOOT-INF中，copy文件夾lib到指定目錄下，如jar包運行目錄；如圖3，


3、分離靜態文件：在lib同目錄下創建resource文件夾，進入classes文件夾內copy文件夾static及templates文件夾到resource文件下；如圖：

4、刪除jar包及解壓文件，當前目錄結構如下：

5、增量打包，打包不再將引用jar及static文件夾、templates文件夾打到jar包中：首先修改pom.xml文件中打包相關配置，如下圖:
打包配置增加了如下代碼：
resource打包配置增加如下過濾：
最終pom.xml中打包配置如下：
6、執行maven clean install,獲得最終jar包，如下圖所示，只有5M大小；

7、最終運行時，jar的執行命令中增加lib及resource的路徑指向，否則項目無法正常運行；
8、如上進行增量打包後，如果前端有不涉及到後端的修改時都可以對resource中的文件進行替換進行實時更新，不再進行重啓；後端有變動也不用上傳100多M的jar到服務器，影響效率；


近日，Apache Dubbo 發佈了 3.3 分支大版本 3.3.0-beta.1，相較於 3.2 系列版本，3.3.0-beta 引入了一些重量級的功能升級，按照社區規劃，3.3 也將是 Dubbo3 非常重要的一個里程碑大版本，在 3




原文地址：https://www.baeldung.com/spring-boot-testing
1 概覽
在這個教程中，我們會帶你看看如果使用 Spring Boot 中的框架編寫測試用例。內容會覆蓋單元測試，也會有在執行測試用例




總有人問JeecgBoot何時支持jdk17和springboot3，目前官方已經推出了SpringBoot 3分支，大家可以提前下載體驗
https://github.com/jeecgboot/jeecg-boot/tree/sprin




本文分享自華爲雲社區《服務運行時動態掛載JavaAgent和插件——Sermant熱插拔能力解析》，作者：華爲雲高級軟件工程師 欒文飛
一、概述
Sermant是基於Java字節碼增強技術的無代理服務網格，其利用Java字節碼增強技術，爲




如果你是企業經營者，在爲企業降本增效而發愁；
如果你是企業的開發、運維或架構同學，在日常工作中被開發效率、交付問題等困擾…… 歡迎來了解 Koupleless（原 SOFAServerless）！
現在，Koupleless 重磅發佈了




作者：饒子昊、楊龍
應用複雜度提升，根因定位困難重重
隨着軟件技術發展迭代，很多企業軟件系統也逐步從單體應用向雲原生微服務架構演進，一方面讓應用實現高併發、易擴展、開發敏捷度高等效果，但另外一方面也讓軟件應用鏈路變得越來越長，依賴的各種外部




背景介紹
應用安裝包的體積影響着用戶下載量、安裝時長、用戶磁盤佔用量等多個方面，據Google Play統計，應用體積每增加6MB，安裝的轉化率將下降1%。
安裝包的體積受諸多方面影響，針對dex、資源文件、so文件都有不同的優化策略，在




一、平臺介紹
財務自營計費主要承接京東自營數據在整個供應鏈中由C端轉B端的功能實現，在整個供應鏈中屬於靠後的階段了，系統主要功能是計費和向B端的彙總。
二、問題描述
近年來自營計費數據量大增，有百億+的數據量，一天中彙總佔據了一半的數據




本文分享自華爲雲社區《應用安全防護ESAPI》，作者： Uncle_Tom。
1. ESAPI 簡介
OWASP Enterprise Security API (ESAPI）是一個免費、開源的web應用程序安全控制庫，使程序員更容易編寫




版本依賴
1. spring-kafka: 2.2.2
2. kafka-clients: 2.0.0
使用示例
1. 構建監聽，acknowledgingMessageListener 爲接口org.springframework.k




 
Automotive Android OS多屏多窗口
DisplayAreaPolicy.Provider
    DisplayAreaPolicy用戶設置DisplayArea的層級結構。DisplayAreaPolicy.Pr




一.背景
性能優化是一場永無止境的旅程。
到家門店系統，作爲到家核心基礎服務之一，門店C端接口有着調用量高，性能要求高的特點。
C端服務經過演進，核心接口先查詢本地緩存，如果本地緩存沒有命中，再查詢Redis。本地緩存命中率99%，服務性




暢捷通介紹
暢捷通是中國領先的小微企業財稅及業務雲服務提供商，成立於2010年。暢捷通在2021年中國小微企業雲財稅市場份額排名第一，在產品前瞻性及行業全覆蓋方面領跑市場，位居中國小微企業雲財稅廠商矩陣領軍象限前列。作爲專注小微企業雲服務




java -cp h2-1.4.200.jar org.h2.tools.Recover
java -cp h2-1.4.200.jar org.h2.tools.Recover -db h2
java -cp h2-1.4.200.




 
前臺js window.atob(); window.btoa()； 後臺 import java.io.UnsupportedEncodingException; import java.net.URLDecoder; import

