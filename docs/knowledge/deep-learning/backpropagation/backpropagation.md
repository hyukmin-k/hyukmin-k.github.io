---
layout: post
title: Backpropagation
nav_order: 1
has_children: true
grand_parent: Knowledge
parent: Deep Learning
permalink: /docs/knowledge/deep-learning/backpropagation
---

# Backpropagation
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Introduction
* 계산그래프(Computational Graph) 노드별 backpropagation 정리

# Backpropagation for computational graph node types

## Matrix Multiplication Node
- $\mathbf{y=xW}$
  - $\mathbf{x}$: $l \times m$ matrix
  - $\mathbf{W}$: $m \times n$ matrix
  - $\mathbf{y}$: $l \times n$ matrix 
- $\frac{\partial L}{\partial \mathbf{x}} = \frac{\partial L}{\partial \mathbf{y}}\cdot \mathbf{W}^T$
- $\frac{\partial L}{\partial \mathbf{W}} = \mathbf{x}^T \cdot \frac{\partial L}{\partial \mathbf{y}}$

### Matrix Calculus
- $\frac{\partial y}{\partial \mathbf{M}} = \begin{pmatrix} \frac{\partial y}{\partial \mathbf{M}_{11}} & \frac{\partial y}{\partial \mathbf{M}_{12}} & \cdots & \frac{\partial y}{\partial \mathbf{M}_{1n}} \\
 \vdots  & \vdots & \ddots & \vdots \\
 \frac{\partial y}{\partial \mathbf{M}_{m1}} & \frac{\partial y}{\partial \mathbf{M}_{m2}} & \cdots & \frac{\partial y}{\partial \mathbf{M}_{mn}} \end{pmatrix}$

# References
- [CS231n: Convolutional Neural Networks for Visual Recognition Spring 2018](http://cs231n.stanford.edu/2018/)
