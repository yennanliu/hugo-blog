
+++
title = '大數據入門（七）win10上eclipse使用Hadoop的配置'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more-->

1、jdk1.8
2、hadoop2.8.3
3、hadoop-eclipse-plugin-2.8.5.jar
【獲取hadoop2x-eclipse-plugin的可以參考(release文件夾下):https://github.com/DoubleBirdsU/Hadoop-eclipse-plugin】
1、 將hadoop-eclipse-plugin-2.8.5.jar，複製到eclipse安裝目錄下的plugins下。如：D:\ProgramFiles (x86)\eclipse\plugins
2、 重啓Eclipse。
3、 點擊菜單欄Windows —>Preferences ，如果插件安裝成功，就會出現：
如果沒成功，首先查看版本是否正確。
其次可以，通過cmd到eclipse的目錄下啓動Eclipse：eclipse.exe -clean
4、選擇，hadoop安裝目錄：D:\Learning\Hadoop\hadoop-2.8.5（這個是我自己的）

新建這個窗口只是爲了可視化hdfs，操作方便，如果覺得不需要，可以跳過5這步，也可以通過網頁查看hdfs：
查看集羣狀態：http://localhost:8088
查看Hadoop狀態：http://localhost:50070/explorer.html#/
5、點擊Windows —>Show View —>Others —>Map/Redure Location —>open,最下面就會出現這個：

點擊Map/Redure Locations 窗口，空白處右鍵New Hadoop location :

這裏會有報錯，原因是hdfs 裏面還沒有input和output目錄:

解決方法是創建input和output文件夾，下圖是創建input的例子:

關於hdfs的基本操作可我的上一篇文章：大數據入門（六）win10對Hadoop hdfs的基本操作（傳送門）
重啓eclipse，沒有報錯：

那麼接下來可以進行一些實驗啦：
大數據入門（八）win10下的wordcount
大數據入門（九）基於win10的Hadoop，java代碼進行hdfs操作
關於Eclipse安裝插件後沒有任何反應的解決
windows10上使用Eclipse配置Hadoop開發環境詳細步驟+WordCount示例
hadoop 2.8.3 eclipse 插件
Eclipse安裝Hadoop插件配置Hadoop開發環境


大家好，我們騰訊位置服務智慧景區團隊爲成都熊貓基地量身打造的官方小程序正式發佈上線啦！
我們以微信小程序端原生的地圖能力，提供了集地圖導覽、主題地圖、攻略規劃在內的旅遊助手產品，幫助景區全面提升遊客體驗！誠邀各位開發者體驗，




隨着大數據時代的來臨，知識圖譜在各個領域的應用越來越廣泛，如智能客服、智能推薦、智能問答等。而OpenSPG作爲一款強大的知識圖譜構建工具，一直備受關注。近日，OpenSPG發佈了新版，帶來了大模型知識抽取和快速知識圖譜構建等功能，進一步提




近日，神策數據作爲專業的大數據分析與營銷科技服務提供商，憑藉着多年數字化實踐沉澱以及服務 30+ 行業客戶的深厚積累，列入 Forrester《2024Q1 亞太地區 CDP Landscape（The Customer Data Pla




松下集團在中國及東北亞地區擁有有64家法人公司，員工人數約4萬人，業務範圍涉及研究開發，養老、鑄件、汽車、車載、能源、電池等多個方面，這些多元化的業務組合爲松下常年可持續性發展提供堅實保障。中國地區的松下已有30多年的歷史，集合了研發、生產




10 月 31 日，杭州雲棲大會上，日誌服務 SLS 研發負責人簡志和產品經理孟威等發表了《日誌服務 SLS 深度解析：擁抱雲原生和 AI，基於 SLS 的可觀測分析創新》的主題演講，對阿里雲日誌服務 SLS 產品服務創新以及背後的技術積累




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

