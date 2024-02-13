
+++
title = '【轉載】Overview of gradient descent algorithms'
date = 2024-02-12T15:50:58
draft = false
+++
<!--more-->Overview of gradient descent algorithms
 
 
Gradient descent is the preferred way to optimize neural networks and many other machine learning algorithms but is often used as a black box. This post explores how many of the most popular gradient-based optimization algorithms such as Momentum, Adagrad, and Adam actually work.
Read more posts by this author.
SEBASTIAN RUDER
19 JAN 2016 • 28 MIN READ
 
This post explores how many of the most popular gradient-based optimization algorithms actually work.
Note: If you are looking for a review paper, this blog post is also available as an article on arXiv.
Update 20.03.2020: Added a note on recent optimizers.
Update 09.02.2018: Added AMSGrad.
Update 24.11.2017: Most of the content in this article is now also available as slides.
Update 15.06.2017: Added derivations of AdaMax and Nadam.
Update 21.06.16: This post was posted to Hacker News. The discussion provides some interesting pointers to related work and other techniques.
Table of contents:
Gradient descent is one of the most popular algorithms to perform optimization and by far the most common way to optimize neural networks. At the same time, every state-of-the-art Deep Learning library contains implementations of various algorithms to optimize gradient descent (e.g. lasagne's, caffe's, and keras' documentation). These algorithms, however, are often used as black-box optimizers, as practical explanations of their strengths and weaknesses are hard to come by.
This blog post aims at providing you with intuitions towards the behaviour of different algorithms for optimizing gradient descent that will help you put them to use. We are first going to look at the different variants of gradient descent. We will then briefly summarize challenges during training. Subsequently, we will introduce the most common optimization algorithms by showing their motivation to resolve these challenges and how this leads to the derivation of their update rules. We will also take a short look at algorithms and architectures to optimize gradient descent in a parallel and distributed setting. Finally, we will consider additional strategies that are helpful for optimizing gradient descent.
Gradient descent is a way to minimize an objective function J(θ)J(θ) parameterized by a model's parameters θ∈Rdθ∈Rd by updating the parameters in the opposite direction of the gradient of the objective function ∇θJ(θ)∇θJ(θ) w.r.t. to the parameters. The learning rate ηη determines the size of the steps we take to reach a (local) minimum. In other words, we follow the direction of the slope of the surface created by the objective function downhill until we reach a valley. If you are unfamiliar with gradient descent, you can find a good introduction on optimizing neural networks here.


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

