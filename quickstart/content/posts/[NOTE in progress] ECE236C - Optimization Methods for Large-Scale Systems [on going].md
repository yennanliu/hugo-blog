
+++
title = '[NOTE in progress] ECE236C - Optimization Methods for Large-Scale Systems [on going]'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more-->Outline
- ∇^2(f (x) )> 0 is not necessary for strict convexity (cf., f (x) = x^4) but sufficient
- a differentiable function f is convex if and only if dom f is convex and (∇ f (x) − ∇ f (y)) ^T (x − y) ≥ 0 for all x, y ∈ dom f i.e., the gradient ∇ f : Rn → Rn is a monotone mapping
- Lipschitz Continuity 即利普希茨連續條件，是一個比通常連續更強的光滑性條件。 直覺上，利普希茨連續函數使用dual norm限制了函數改變的速度（從效果上感覺與限制二階導數ub類似），符合利普希茨條件的函數的斜率，必小於一個稱爲利普希茨常數的實數（該常數依函數而定）。
- ||∇ f (x) − ∇ f (y)||∗ ≤ L||x − y|| for all x, y ∈ dom f 則f爲L-smooth。此處的dual norm ,定義是對於所有normed vector v，線性關係zv的模的最大值。並且易見：
- Convexity vs Strict Convexity vs Strong Convexity (更加凸) (wiki)

- By using the property of convexity and Lipschitz continuity, upper and lower bound of f(x+delta) can be proved with a quadratic term. The equations reminds the second order Taylor approximation. After that, it can be proved by choosing step size smartly, gradient decent does the work at each iteration.


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

