---
layout: default
title: Feature Point
nav_order: 1
has_children: true
grand_parent: Knowledge
parent: Computer Vision
permalink: /docs/knowledge/computer-vision/feature-point
---

# Feature Point
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Introduction
* 이미지들 사이에 대응점을 찾기 위한 방법으로 이미지에서 구별이 용이한 특징점들을 찾아내고(Feature Detection) 해당 특징점의 특징을 기술하여(Feature Description) 대응점을 찾아내는(Feature Matching) 방법들을 사용함

* ![feature_building](./feature_building.jpg)
  * E, F가 구별이 용이함

---
# Feature Detection
* 특징점의 후보로 corner 점들을 들 수 있으며 이를 검출하기 위한 Harris corner detector와 이를 개선한 Shi-Tomasi corner detector 등이 있음
  * 회전과 이동 변환에 불변이나 scale 변환에 약함
* David Lowe 가 스케일 변환에 불변인 SIFT 알고리즘을 만들었으며 이의 성능향상 버전인 SURF도 나옴
  * SIFT는 기술돌파로 평가되고 있으며 현재에도 좋은 성능을 나타내고 있음 (2019년 9월 인용횟수 52569회로 컴퓨터 비전분야 1위임)
  * SURF는 SIFT 대비 3배 정도의 속도향상이 있다고 함 
  * SIFT, SURF 모두 특허가 있어 사용 시 주의해야 함
  * SIFT, SIRF 모두 descriptor 도 제공함
* 실시간 성이 중요해지면서 속도가 빠른 FAST 등장
  * FAST는 검출 알고리즘만 제시하며 주로 binary descriptor들과 함께 쓰임
  * 스케일 변환에는 약함
* OpenCV를 관리하던 연구소에서 ORB를 만듦
  * FAST를 피라미드화한 영상에 적용하여 스케일 변환에 대비
  * 방향을 가진 BRIEF 기술자를 사용하여 회전변환에 불변
  * SIFT, SURF를 대체하기 좋음 
## SIFT (Scale-Invariant Feature Transform)
* 소개
  * 

1. ![Scale invariance](sift_scale_invariant.jpg)
1. ![Difference of Gaussian](./sift_dog.jpg)
1. ![Local extrema](./sift_local_extrema.jpg)

## SURF (Speeded-Up Robust Features)
## FAST (Features from Accelerated Segment Test)
## ORB (Oriented FAST and Rotated BRIEF)

---
# Feature Description


## BRIEF (Binary Robust Independent Elementary Features)
## ORB (Oriented FAST and Rotated BRIEF)
## BRISK (Binary Robust Invariant Scalable Keypoints)


---
# Feature Matching


---
# Applications

## AR

## Photogrammetry

---
# References
* [OpenCV docs](https://docs.opencv.org)
* [Basics of AR: Anchors, Keypoints & Feature Detection](https://www.andreasjakl.com/basics-of-ar-anchors-keypoints-feature-detection/)
* [Basics of AR: SLAM – Simultaneous Localization and Mapping](https://www.andreasjakl.com/basics-of-ar-slam-simultaneous-localization-and-mapping/)
