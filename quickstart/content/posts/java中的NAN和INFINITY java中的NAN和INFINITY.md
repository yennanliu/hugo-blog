
+++
title = 'java中的NAN和INFINITY java中的NAN和INFINITY'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more--> 
 
java浮點數運算中有兩個特殊的情況：NAN、INFINITY。
1、INFINITY：
在浮點數運算時，有時我們會遇到除數爲0的情況，那java是如何解決的呢？
我們知道，在整型運算中，除數是不能爲0的，否則直接運行異常。但是在浮點數運算中，引入了無限這個概念，我們來看一下Double和Float中的定義。
Double：
 
Float：
 
那麼這些值對運算會有什麼影響呢？
我們先思考一下下面幾個問題：
1.無限乘以0會是什麼？
2.無限除以0會是什麼？
3.無限做除了1、2、3外的運算結果是什麼？
 1. 無限乘以0，結果爲NAN
 2.無限除以0，結果不變，還是無限
 3.無限做除了乘以0意外的運算，結果還是無限
 
要判斷一個浮點數是否爲INFINITY，可用isInfinite方法
 
2、NAN
java中的NAN是這麼定義的：
 
NAN表示非數字，它與任何值都不相等，甚至不等於它自己，所以要判斷一個數是否爲NAN要用isNAN方法：
System.out.println(Float.NaN == Float.NaN); // output: falseSystem.out.println(Double.isNaN(Float.NaN)); // output: true
 
 
 


 
ThreadLocal的使用，，，實際上相當於維護了一個Map，其中以鍵值對的形式，存儲了某一個數據被多個線程訪問所對應的值。當然這個數據只能有




寫在前面：2020年面試必備的Java後端進階面試題總結了一份複習指南在Github上，內容詳細，圖文並茂，有需要學習的朋友可以Star一下！
GitHub地址：https://github.com/abel-max/Java-S




一致性協議有很多種，比如 Paxos，Raft，2PC，3PC等等，在這講一種協議，ZAB 協議，該協議應該是所有一致性協議中生產環境中應用最多的了。爲什麼？因爲它是爲 Zookeeper 設計的分佈式一致性協議！
1. 什麼是




寫在前面：2020年面試必備的Java後端進階面試題總結了一份複習指南在Github上，內容詳細，圖文並茂，有需要學習的朋友可以Star一下！
GitHub地址：https://github.com/abel-max/Java-S




Spring 早已成爲 Java 後端開發事實上的行業標準，無數的公司選擇 Spring 作爲基礎的開發框架，大部分Java 後端程序員在日常工作中也會接觸到 Spring ，因此，如何用好 Spring ，也就成爲 Java




Array
Array 含有sort、fill、equals、BinarySearch等方法
import java.util.Arrays;
import java.util.Random;
public class Arra




springboot部署打包爲jar，一般都是全量打包，jar包的大小通常都是超過100M的，並且在進行一般的頁面html微調、js修改、img替換、css樣式修改時也需要重新打包進行部署；每次微小的調整都需要重新打包就太煩了，一




項目需要增加聊天會話功能，涉及到上傳語音圖片等信息。考慮新增一個目錄，所有相關文件存在一個相同的目錄中。因此需要對原項目增加一個存儲的路徑。以前的項目因爲只有一個路徑，且已經運行中。走了些彎路，僅此記錄操作過程。nginx version




 JSONArray序列化日期最初用到， 這個是全局設置，會有風險。
    String[] dateFormats = new String[] {"yyyyMMdd"};
                JSONUtils.getM




直接上源碼，定義一個抽象類，必須實現get方法。該方法是用來獲取需要緩存的對象的。 
import java.util.HashMap;
import java.util.Map;
/**
* 用於從數據庫中獲取相應值的緩存類
*




Java程序中對類的使用方式分爲兩類 ：主動使用和被動使用
主動使用：
創建類的實例
訪問某個類或接口的靜態變量，或者對該靜態變量賦值
調用類的靜態方法
反射
初始化一個類的子類
java虛擬機啓動時被標明爲啓動類的類
從JDK




目錄工具eclipse的Hadoop環境配置參考
系列：
大數據入門（一）環境搭建，VMware15+CentOS8.1 配置
https://blog.csdn.net/qq_34391511/article/details/1




如題，直接帶入案例進行理解Java的動態綁定機制，不多說直接上代碼了。
package one;
public class JavaTest {
public static void main(String[] args




在Linux實操的過程中，你是否有過這些疑問：
如何提取日誌中含有關鍵字的指定行，上一行或上幾行？
ln 做了符號鏈接，對符號鏈接進行權限修改，原文件是否會受到影響？
Shell 腳本里有很多特殊符號，到底該怎麼用？網上流傳的

