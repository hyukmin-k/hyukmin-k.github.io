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
- $y=xW$
  - $x$: $l \times m$ matrix
  - $W$: $m \times n$ matrix
  - $y$: $l \times n$ matrix 
- $\frac{\partial L}{\partial x} = \frac{\partial L}{\partial y}\cdot W^T$
- $\frac{\partial L}{\partial W} = x^T \cdot \frac{\partial L}{\partial y}$


# References
- [CS231n: Convolutional Neural Networks for Visual Recognition Spring 2018](http://cs231n.stanford.edu/2018/)
