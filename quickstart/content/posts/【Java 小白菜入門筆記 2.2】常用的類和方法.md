
+++
title = '【Java 小白菜入門筆記 2.2】常用的類和方法'
date = 2024-02-10T23:02:01
draft = false
+++
<!--more-->Array 含有sort、fill、equals、BinarySearch等方法
輸出結果：
注意：binarySearch只能用於已經排序的數組。如返回正數，爲所在位置。如果找不到，則爲負數，其絕對值表示這個數應該被插入的位置。
StringBuilder是一個可以insert、delete、replace、append字符串中元素的一個可變的對象。內置了很多字符串操作的相關方法。StringBuilder可以通過toString方法轉爲String類型。下面是一個例子：
輸出爲：
Math在java.lang中，實現了很多常用的數學函數，比如sin、cos等三角、反三角函數，以及ceil、floor、rint等不同的double取整方式，以及pow計算冪，以及random生成隨機數等。
通過一個例子，來使用一下Math中的常見函數：
輸出結果：
注意：rint和round的區別在於，rint返回的仍是double，而round對於double返回的是long，對float返回int。都是返回最接近的整數值。
實驗，random兩個數，比較大小：
輸出結果：
System不能被實例化，只能訪問static方法。常用的System.out.println就是System 的一個方法。
實驗案例：
輸出結果：
實驗：輸入一個m和一個n，其中m小於n，兩者都是正整數，輸出一個[m, n]範圍內的隨機數。
輸入輸出爲：
2020年7月8日00:58:49
北京 生命科學園


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




近日，Apache Dubbo 發佈了 3.3 分支大版本 3.3.0-beta.1，相較於 3.2 系列版本，3.3.0-beta 引入了一些重量級的功能升級，按照社區規劃，3.3 也將是 Dubbo3 非常重要的一個里程碑大版本，在 3




 
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




相信近期從事基礎設施工作的各位，對 IT 成本治理，以及 FinOps 體系的概念已經有了一些認知。在 Google 近 5 年的熱度趨勢中，FinOps 的趨勢也在持續上升。
在阿里雲的同學與客戶實際工作協同中，我們發現成本治理是幾乎每位




一、什麼是SQL
sql(Structured Query Language: 結構化查詢語言)是高級的費過程化編程語言,允許用戶在高層數據結構上工作, 是一種數據查詢和程序設計語言, 也是(ANSI)的一項標準的計算機語言. but...

