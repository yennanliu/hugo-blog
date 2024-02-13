
+++
title = '[NOTE in progress] Simulation Optimization'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more-->簡單記錄一下關於仿真優化的一些知識點和思考。主要基於：Handbook of Simulation Optimization, Michael Fu
Table of Contents
Overview
Discrete Optimization
Three fundamental type of errors:
Optimality Conditions
Different scenarios depending on the solution space size:
Ranking and Selection
Ordinal Optimization (OO)
Globally Convergent Adaptive Random Search
Locally Convergent Adaptive Random Search
Commercial Solvers
這是本書的overview 實際上也可以看做是這一field的overview.
一種分類方式：Discrete vs Continuous
Since stochasticity is the keyword, some base knowledge is important for DO as well as for CO.
Two formulations are concerned: 
IZF (Frequentist)
Assume  which is the most difficult case. The objective is to find x1 which is at least -better than all the others.
Based on the principle of the above 3 procedures, further procedures include:
BF (Bayesian) (Does not provide PSC guarantees)
Used when prior information is available.
Helps to choose the next solution to explore, based on prior information and previous sample results, and also the simulation budgets. This involves a MDP problem and can be possibly solved by ADP/RL.
Conclusion
Brankle et al. found that no R&S procedure is dominent in all situations. (thousands of pb structures tested). BF is often more efficient in terms of nb of samples, but it doesn't provide correct-selection optimality guarantee like frequentist does.
When the solution space is large, OO proposes "sofe optimization", which selects a subset S from  and limit the analysis to S. We are interested in the probability that , where T is the set of top t solutions in the whole space.  is called the alignment level and the probability is alignment probability.
Two basic idea behind OO:
OO is more an analysis than new algorithm, the procedure will be:
In practical i don't think this is so interesting, since it just tells you that, the larger  is, the better.
Designed for large but finite solution space. Guarantee 
Generic GCARS:
Several algoritms are described:
Similar to GCARC, but with a statistical procedure to test the local optimality of .
COMPASS (Convergen Optimization via Most-Promising-Area Stochastic Search)
 
AHA (Adaptive Hyperbox Algo)
Like COMPASS, but define the neighborhood as the hyperbox around x* :  where d is the dimension of x.
Most simulation modeling softwares includes SBO tool, but most of them are based on R&S or meta-heuristics like SA. Meta-heuristics have been observed to be effective on difficult deterministic optimization problems but they usually provide no performance guarantees. Some advises are:
Most of the above mentioned algorithms are black-box algorithms that do not depend on problem structures. This can be considered in defining the neighborhood in LCRS, for instance.
 
 
 


直播概要：
隨着計算機的蓬勃發展，互聯網進入大數據和人工智能時代，爲了解決信息過載和長尾商品，推薦系統成爲唯一選擇，而面對不同的業務場景，爲了解決業務痛點，會根據不同的場景特點尋找不同的方法和手段來解決推薦中實際遇到的問題。在智慧家庭領域，




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"blockquote","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null}},{"type":"blockq




{"type":"doc","content":[{"type":"blockquote","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null}},{"type":"blockq




{"type":"doc","content":[{"type":"blockquote","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null




{"type":"doc","content":[{"type":"blockquote","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null




{"type":"doc","content":[{"type":"paragraph","attrs":{"indent":0,"number":0,"align":null,"origin":null},"content":[{"typ

