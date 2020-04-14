```bash
---
layout:     post
title:      与 SVM 的第一次邂逅
subtitle:   春天的一次组会
date:       2020-04-14
author:     WC
header-img: img/svm-back.jpg
catalog: true
tags:                               #标签
    - machine learning
---

```

# 与 SVM 的第一次邂逅

## Overview

This repository complements the paper [Missing Data Imputation using Optimal Transport](http://arxiv.org/abs/2002.03860) (Muzellec B., Josse J., Boyer C., Cuturi, M.):

<img src="https://i.loli.net/2020/04/14/WLjlVJBvc96wR1D.png" alt="幻灯片1.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/gnxRyEkYTMCPuZr.png" alt="幻灯片2.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/21nhOQVLizUklpc.png" alt="幻灯片3.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/hVXiuwB1nklmcQM.png" alt="幻灯片4.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/YeHLVMNcsSRlGby.png" alt="幻灯片5.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/WFpRtQAPGuk3s4V.png" alt="幻灯片6.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/Xs7mchYbiASoPqv.png" alt="幻灯片7.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/VdAn5IOu2gNkKUW.png" alt="幻灯片8.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/REhF6HZWTdQb9uc.png" alt="幻灯片9.PNG" style="zoom:50%;" />

<img src="https://i.loli.net/2020/04/14/c9YQqzUjtE6fRTk.png" alt="幻灯片10.PNG" style="zoom:50%;" />





- `experiment.py` allows to reproduce the imputation benchmark therein;
- `imputers.py` contains the classes corresponding to algorithms 1 and 3;
- `data_loaders.py` contains data loading utilities for the UCI ML repository datasets on which experiments are run;
- `utils.py` contains methods of general utility, and the implementation of MAR and MNAR missing data mechanisms in particular;
- `softimpute.py` contains the implementation of the softimpute baseline.

## References

Muzellec B., Josse J., Boyer C., Cuturi, M.: [Missing Data Imputation using Optimal Transport](http://arxiv.org/abs/2002.03860)

## Dependencies
- [PyTorch](https://pytorch.org/)
- [GeomLoss](https://www.kernel-operations.io/geomloss/)
- [POT](https://pot.readthedocs.io/en/stable/)

To use the data loading utilities in `data_loaders.py`, [wget](https://pypi.org/project/wget/) is also required.
