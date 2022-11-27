# Monopoly

## Intro our game
> **「買地吧，因為土地已經停產了！」 -- 馬克·吐溫（Mark Twain）**

![大富翁地圖|1934×2067, 60%](https://user-images.githubusercontent.com/29699103/203911488-8d0c9c89-c67c-478f-99b0-8cb72ce720f0.jpg)
家喻戶曉的桌遊**Monopoly**，又名大富翁或地產大亨，其最早可追朔至伊莉莎白．馬吉(Elizabeth Magie)設計的地主遊戲(the Landlord’s Game)。

最初的地主遊戲有兩種玩法：「繁榮」和「壟斷」，兩種玩法旨在傳達不同的產權制度會造成不同的社會結果，她呼籲國家應對土地徵稅，稅金收入的使用應考量所有人的利益，進而達到共存共榮，「繁榮」玩法的勝利條件為：當資金最少的玩家資金翻倍時，所有人接獲勝；反之「壟斷」則是為了勸世，放任土地私有終將走向貧富差距越來越大的後果(在遊戲中的結局即是除一人外所有人皆破產)。

然而從Monopoly這個名字可以察覺到，現今大家所知的遊戲，只保留了「壟斷」的玩法，當時一個名叫查爾斯·達羅(Charles Darrow)的失業人士修改了遊戲規則並將遊戲賣給「帕克兄弟」(Parker Brothers，一家美國的遊戲公司)。

諷刺的是，這個行為就像是「壟斷」玩法的主旨：如果想出人頭地，那就要追逐財富，碾壓對手。
+ 參考資訊：
	+ [她發明了史上最暢銷的桌遊「大富翁」　結局卻是名譽被盜、遊戲初衷背道而馳](https://www.upmedia.mg/news_info.php?Type=5&SerialNo=105535)
	+ [《大富翁》遊戲初衷是想證明資本主義邪惡](https://www.bbc.com/ukchina/trad/vert-cap-41087496)
	+ [《大富翁》遊戲初衷非「買地賺大錢」 而是諷刺邪惡的資本主義](https://www.businesstoday.com.tw/article/category/80407/post/201811170004/)
	+ [买地吧！因为土地已经停产了](https://zhuanlan.zhihu.com/p/89021467)


### 遊戲規則概述
+ 2 - 4 人
+ 道具：
	+ 地圖
	+ 骰子
	+ 房子
	+ 地契
	+ 貨幣
+ 初始配置
	+ 每個玩家擲骰子決定先後次序，點數大的玩家先行，之後再以順時針方向進行
	+ 在遊戲開始前，每個玩家都會獲得初始金額
+ 玩家依序擲骰、移動到目標格(以下以**已移動到目標格**為前提進行說明)
+ 玩家在自己的回合內：
	+ **購買土地**：若是到達該土地或車站沒有地主，可選擇購買
	+ **支付過路費**：若到達他人土地，則必須支付過路費[^1]
	+ **蓋房子**：若到達自己的土地，可以選擇蓋房子，一次只能蓋一棟，一塊土地上最多擁有5棟房子
	+ **停車場**：若到達停車場，該輪無法向其他玩家收取過路費
	+ **監獄**：若玩家到達監獄，則下一輪略過該玩家，在離開監獄之前，無法向其他玩家收取過路費
	+ **拍賣**：玩家可以自行選擇拍賣自己擁有的房地產[^2] 
	+ **抵押**：玩家可以自行選擇抵押自己擁有的房地產，若限定回合內無法贖回，則失去該房地產的擁有權
	+ **破產**：若無法支付過路費，必須透過拍賣或抵押籌措，如果全數抵押或拍賣仍無法支付，則該玩家宣告**破產**
+ 玩家在經過起點時可以獲得獎勵金！！ 但是剛好踩在上面的話沒有
+ 遊戲結束：
    1. 除一人以外所有玩家皆破產，該玩家獲勝
    2. 遊戲時間結束，總資產最多的玩家獲勝

## 計算

### 過路費

> 過路費 = 土地空地價 * 房子數量 * 同地段數量 * 是否坐牢/停車場休息(0/1)

#### 房子數量

| 數量 | 係數 |
| ---- | ---- |
| 0    | 0.05 |
| 1    | 0.4  |
| 2    | 1    |
| 3    | 3    |
| 4    | 6    |
| 5    | 10   |

#### 同地段數量

| 數量 | 係數 |
| ---- | ---- |
| 1    | 1    |
| 2    | 1.3  |
| 3    | 2    |
| 4    | 4    |
| 5    | 8    |
| 6    | 16   |

## 抵押

* 房地產價值的70%

## 拍賣

* 初始金額 = 房地產價值的50%
* 流標時系統回收價 = 房地產價值的70%

[^1]: **過路費**：每塊土地的過路費金額會受：土地購買費、該土地房子數量、該玩家擁有多少相同地段土地等因素影響，而車站的過路費金額僅受該玩家擁有多少車站影響
[^2]: **房地產**：土地和房子的總稱

## My Practice Stack
- 描述一下你們使用的軟體方法論 :
    * Event Storming
    * Example Mapping
    * OOAD
    * ATDD
    * DDD
    * Clean Architecture

#### Tech Stack
- 描述一下你們使用的技術、框架、語言 :
    * C#/.Net
    * MongoDB
    * Blazor
    * SignalR