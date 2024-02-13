
+++
title = 'An Overview of Reinforcement Learning'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more-->強化學習概覽
This overview is largely based on this article: https://medium.com/@SmartLabAI/reinforcement-learning-algorithms-an-intuitive-overview-904e2dff5bbc.
 
[source:https://www.quora.com/Why-is-Q-Learning-deemed-to-be-off-policy-learning]
主要判斷，在更新Q時，涉及到的Q(s',a')中的a'是否由當前actor根據s'得出,抑或是一種approximation like the max function in q-learning. 在使用replay-buffer的情況下，或者a'由target actor生成的情況下，稱爲off-policy。否則是on-policy。這是我個人瀏覽了很多信息後，目前的理解。[update 0413]見下圖，目前有了新的理解：remember Qfunction是基於TD的，前後action是有順序關係的。換句話說，train Q的時候，需要知道，是Q(?)跟當前的Q差了一個r。這時，如果此處的？與當前policy應當輸出的action相符，說明我們想要把Q 按照當前policy去train，所以是on policy。否則的話，如Sarsa，當前policy給出的是epsilon-greedy choice但是train Q的時候假定下一步是totally greedy的，所以Q與當前policy不符合，所以是off。
涉及到replay buf時候，relay-buffer給出的a'是歷史上的某個policy的action，與當前actor所能返回的action不同，所以Q沒有在試圖把自己train成當前policy的評估函數，所以是off。
總結：判斷on還是off，取決於，train Q的時候，Q(s',a')中的a'與當前actor所建議的action是否相同。換句話說，我們是否在把Q train成當前police的評估函數。
 

那麼下一個問題來了：兩者應該如何選擇呢？下面這個回答可以參考一下，特別是對於'take action'的理解。所以總的來說q learning off policy直接learn optimal policy但是有可能會不穩定，難以converge等。Sarsa相對conservative一些，所以當training代價比較大時可以考慮。

最後一個疑問，今天意識到TD本質上是有時間順序在的：Q(s,a) for a->a'->a'' 和 Q(s,a) for a->a''->a'兩者的值可能本來就不能一致。針對TD背後的思想，需要進一步思考
On-policy v.s. Off-policy
An on-policy agent learns the value based on its current action a derived from the current policy, whereas its off-policy counter part learns it based on the action a* obtained from another policy.
The reason that Q-learning is off-policy is that it updates its Q-values using the Q-value of the next state s′ and the greedy action a′. In other words, it estimates the return (total discounted future reward) for state-action pairs assuming a greedy policy were followed despite the fact that it's not following a greedy policy.
The reason that SARSA is on-policy is that it updates its Q-values using the Q-value of the next state s′ and the current policy's action a′′. It estimates the return for state-action pairs assuming the current policy continues to be followed.
The distinction disappears if the current policy is a greedy policy. However, such an agent would not be good since it never explores.
f(state) -> action.
What action to take now?
Remarks
f(state, action)->expected action value
Action-value functoin: How good is it if an particular action is taken?
Can be used in Control Theory. Environment has assumptions and approximations.
 


Pai-Megatron-Patch是什麼
Pai-Megatron-Patch工具是阿里雲機器學習平臺PAI算法團隊研發，基於阿里雲智算服務PAI-靈駿平臺的大模型最佳實踐解決方案配套工具，旨在幫助大模型開發者快速上手靈駿產品，完成大語




快速成長總共三篇，分別是《完成自我認知升級》、《自我成長好方法》和《自我培養和培養他人》。本篇是第三篇，篇幅較長。針對長文的閱讀方式，依舊建議在《完成自我認知升級》中提到的閱讀方式：“在一個不被打擾的時間做好隻字不差閱讀，用批判性思維思考和




背景
Stable Diffusion（SD）是一種流行的AI生成內容（AI Generated Content，AIGC）模型，能在文字輸入的基礎上生成各種風格多樣的圖像。在目前的AIGC方向，SD是開源社區最熱門的模型。然而，SD能夠




| 嘉賓：吳友政，京東集團高級總監、京東科技語音語言算法部負責人。
2006年中科院自博士畢業後，先後在日本國立信息通信研究機構、英國愛丁堡大學、索尼中國研究院從事自然語言處理相關研究工作，主要聚焦自然語言處理、人機對話、語音識別、機器翻




總結一下自己入坑強化學習的經驗。
在入坑之前，自己對強化學習基本一無所知，所以對於強化學習的學習基本上是從零開始。
下面總結一下自己學習強化學習所看的網課，教材，論文，代碼
網課
莫煩的強化學習教程。這個教程真的是通俗易懂，完全針對初




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"heading","attrs":{"align":null,"level":1},"content":[{"type":"text","text":"前言：","attr




{"type":"doc","content":[{"type":"blockquote","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null




{"type":"doc","content":[{"type":"heading","attrs":{"align":null,"level":1},"content":[{"type":"text","text":"前言","attrs




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




直播概要：
隨着計算機的蓬勃發展，互聯網進入大數據和人工智能時代，爲了解決信息過載和長尾商品，推薦系統成爲唯一選擇，而面對不同的業務場景，爲了解決業務痛點，會根據不同的場景特點尋找不同的方法和手段來解決推薦中實際遇到的問題。在智慧家庭領域，




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"blockquote","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ

