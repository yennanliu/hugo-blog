
+++
title = 'Stochastic Optimization: Casual Notes'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more-->Currently learning stochastic optimization (SO) theory, I will note important content here. Some book references are:
As i understood, the basic form of a two-stage problem:
optimize f(x)+Eξ(min⁡y(w,x)+q(w))f(x) + E_{\xi}(\min y(w,x) + q(w))f(x)+Eξ​(miny(w,x)+q(w))
where xxx is the first-stage decision, while w∈ξw\in \xiw∈ξ is a random event. The objective is to find the optimal FIRST-STAGE decision resulting the best expected profit/cost.
Inherently two-stage: first stage is long term investment and the second stage is short term usage of this investment. Two stage, two different decision types.
Inherently multi-stage: many stages, same type of decision.
Two stage or multi-stage? It depends on the modeler. If the decision is made in a rolling horizon manner, then instead of make a multi-stage model, we may use two-stage as a simplification. Later stages are aggregated since we do not need so much detail.
Non-anticipativity: if two scenarios are indistinguishable before time t, then the action taken at time t on each scenario must be the same.
Horizon effect in multistage SO: some multistage problem has infinite time horizon. When the horizon is long, we are approaching a steady-state, but in SO we only care about the transient decision, so we have to represent the steady state in the model in order to obtain the right transient behavior. We don’t really care what to do far in the future.
To deal with horizon effect, King & Wallace (2012) presented what they call Dual Equilibrium as a tool to consider infinite stead-stage effect into the SO model. Check chapter 2.3.6.
A SO is often solved in its deterministic form based on a number of scenarios generated to describe the uncertainty. To do this, firstly we must generate scenarios correctly.
It’s important to realize, that we pass from random variables to discretization because of the algorithm that we are choosing. So it’s important to ensure that the discretization is not too far from reality W.R.T the ALGORITHM!
Algorithms that do not need scenarios as input
Use scenarios trees as input
Two problems:
Where to sample from : if you do not have reliable information on the true distribution, just use the empirical one !
What is a good discretization?
It depends on the model! Our aim is not to approximate the real distribution, instead, we want the algorithm to feel like using the real distribution.
Approach 1
Approach 2
Replicate the distribution by respecting some important properties like: first moment, second moment, third moment… Use some regression methods to do this or use the iterative procedure provided by King & Wallace (2012).
Approach 3
Generating scenarios by minimizing the distance between the generated one and the real one. This is called scenario reduction methods. It’s used when we somehow know the distribution but want to use minimum number of scenarios to represent it. This must integrate an optimization procedure into the scenario generation module.
Optimality gap estimators


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

