# Revisiting Cross-View Localization from Image Matching
[![Paper](http://img.shields.io/badge/paper-arXiv.2508.10716-B31B1B.svg)](https://arxiv.org/abs/2508.10716)

This paper is currently being revised internally in preparation for submission. We welcome any questions or suggestions via the Issues section.

## ✅ To-Do

- [x] Initial repo structure.
- [ ] Codes and models.
- [ ] CVFM benchmark.

![intro_fig](./figure/intro_fig.jpg)
The top two rows show localization results, with a shared region highlighted in yellow across views; the red box in the top-left image marks a mismatch from the previous method. 
The bottom two rows show matching results, where green and red lines indicate correct and incorrect matches. 
Our method estimates surface height from the ground view, enabling physically consistent cross-view image matching and more accurate localization.

## Abstract:
Cross-view localization aims to estimate the 3 degrees of freedom pose of a ground-view image by registering it to aerial or satellite imagery. It is essential in GNSS-denied environments such as urban canyons and disaster zones. 
Existing methods either regress poses directly or align features in a shared bird’s-eye view (BEV) space, both built upon accurate spatial correspondences between perspectives. 
However, these methods fail to establish strict cross-view correspondences, yielding only coarse or geometrically inconsistent matches. 
Consequently, fine-grained image matching between ground and aerial views remains an unsolved problem, which in turn constrains the interpretability of localization results.
In this paper, we revisit cross-view localization from the perspective of cross-view image matching and propose a novel framework that improves both matching and localization.
Specifically, we introduce a Surface Model to model visible regions for accurate BEV projection, and a SimRefiner module to refine the similarity matrix through local-global residual correction, eliminating the reliance on post-processing like RANSAC. 
To further support research in this area, we introduce CVFM, the first benchmark with 32,509 cross-view image pairs annotated with pixel-level correspondences. 
Extensive experiments demonstrate that our approach substantially improves both localization accuracy and image matching quality, setting new baselines under extreme viewpoint disparity.

