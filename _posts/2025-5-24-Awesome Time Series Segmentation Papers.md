---
title: 'Awesome Time Series Segmentation Papers'
date: 2025-05-24
category: Time Series
permalink: /posts/2025-5-24-Awesome Time Series Segmentation Papers
layout: single
classes: wide
excerpt: "This article contains a reading list of papers on Time Series Segmentation. This article is still being continuously improved.<br/><img src='../images/2025-5-24-Awesome-Time-Series-Segmentation-Papers.png'>"
tags:
  - Time Series Segmentation
  - Machine Learning
---

This article contains a reading list of papers on Time Series Segmentation. This article is still being continuously improved.

<a href="https://www.star-history.com/#lzz19980125/awesome-time-series-segmentation-papers&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=lzz19980125/awesome-time-series-segmentation-papers&type=Date" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=lzz19980125/awesome-time-series-segmentation-papers&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=lzz19980125/awesome-time-series-segmentation-papers&type=Date" />
  </picture>
</a>

## Description

This repository contains a reading list of papers on **Time Series Segmentation**. **This repository is still being continuously improved.**

As a crucial time series preprocessing technique, **semantic segmentation** divides poorly understood time series into several discrete and homogeneous segments. This approach aims to uncover latent temporal evolution patterns, detect unexpected regularities and regimes, thereby rendering the analysis of massive time series data more manageable. 

Time series segmentation often intertwines with research in many domains. Firstly, the relationship between **time series segmentation, time series change point detection,** and some aspects of **time series anomaly/outlier detection** is somewhat ambiguous. Therefore, this repository includes a selection of papers from these areas. Secondly, time series segmentation can be regarded as a process of information compression in time series, hence papers in this field often incorporate concepts from **information theory** (e.g., using minimum description length to guide the design of unsupervised time series segmentation models). Additionally, the task of decomposing human actions into a series of plausible motion primitives can be addressed through methods for segmenting sensor time series. Consequently, papers related to motion capture from the fields of **computer vision** and **ubiquitous computing** are also included in this collection.

Generally, the subjects of unsupervised semantic segmentation can be categorized into:

* **Univariate** univariate time series: 1×T, where T is the length of the time series.
* **Multivariate** multivariate time series: M×T, where M is the number of variables (channels).
* **Tensor** tensor: N₁×⋯×Nₖ×M×T, where N₁×⋯×Nₖ denotes the dimensions other than time and variables.

In the field of time series research, unlike time series forecasting, anomaly detection, and classification/clustering, the number of papers on time series segmentation has been somewhat lukewarm in recent years (this observation may carry a degree of subjectivity from the author). Additionally, deep learning methods do not seem to dominate this area as they do in others. Some classic but solid algorithms remain highly competitive even today, with quite a few originating from the same research group. Therefore, in the following paper list, I will introduce them indexed by well-known researchers and research groups in this field.

## Some Additional Information

🚩 2024/4/28: **In fact, manually annotating segment points (change points) in large time series datasets is extremely labor-intensive and somewhat subjective. Therefore, the field of time series segmentation lacks large public datasets with ground truth, making it difficult for supervised methods to find sources of training data. Unsupervised time series segmentation also acts to some extent as an automatic annotator of segmentation points, making it easier to implement. Currently, 95% of the research work included in this repository is unsupervised.**

🚩 2024/1/27: **I have marked some recommended papers / datasets / implementations with 🌟 (Just my personal preference 😉).**

## Survey & Evaluation

NOTE: the ranking has no particular order.

<div class="table-wrapper">

| TYPE | Venue | Paper Title and Paper Interpretation | Code |
|:---|:---|:---|:---|
| Survey | *Comput. Mater. Con. '24* | Unsupervised Time Series Segmentation: A Survey on Recent Advances | None |
| Dataset | *DARLI-AP@EDBT/ICDT '23* | Time Series Segmentation Applied to a New Data Set for Mobile Sensing of Human Activities 🌟 | [MOSAD](https://github.com/ermshaua/mobile-sensing-human-activity-data-set) |
| Dataset | *ECML-PKDD Workshop '23* | Human Activity Segmentation Challenge@ECML/PKDD'23 🌟 | [Challenge Link](https://ecml-aaltd.github.io/aaltd2023/challenge.html) |
| Visualization | *IEEE TVCG '21* | MultiSegVA Using Visual Analytics to Segment Biologging Time Series on Multiple Scales | None |
| Survey | *IEEE J. Sel. Areas Commun. '21* | Sequential (Quickest) Change Detection Classical Results and New Directions | None |
| Survey | *Signal Process. '20* | Selective review of offline change point detection methods 🌟 | [Ruptures](https://centre-borelli.github.io/ruptures-docs/) |
| Evaluation | *Arxiv '20* | An Evaluation of Change Point Detection Algorithms 🌟 | [TCPDBench](https://github.com/alan-turing-institute/TCPDBench) |
| Survey | *Knowl. Inf. Syst. '17* | A survey of methods for time series change point detection 🌟 | None |
| Evaluation | *Inf. Syst. '17* | An evaluation of combinations of lossy compression and change-detection approaches for time-series data | None |
| Survey | *IEEE Trans Hum. Mach. Syst. '16* | Movement Primitive Segmentation for Human Motion Modeling A Framework for Analysis 🌟 | None |
| Survey | *EAAI '11* | A review on time series data mining | None |
| Survey | *CSUR '11* | Time-series data mining | None |
| Dataset | *GI '04* | Segmenting Motion Capture Data into Distinct Behaviors 🌟 | [Website](http://graphics.cs.cmu.edu/projects/segmentation/) |

</div>

## [David Hallac (Stanford)](https://scholar.google.com/citations?hl=zh-CN&user=o23Mn0cAAAAJ&view_op=list_works&sortby=pubdate)

<div class="table-wrapper">

| TYPE | Venue | Paper Title and Paper Interpretation | Code |
|:---|:---|:---|:---|
| Multivariate | *KDD Workshop MiLeTS '20* | Driver2vec Driver Identification from Automotive Data | [Driver2vec](https://github.com/JingboYang/driver2vec) |
| Multivariate | *Adv. Data Anal. Classif. '19* | Greedy Gaussian segmentation of multivariate time series 🌟 | [GGS](https://github.com/cvxgrp/GGS) |
| Multivariate | *Arxiv '18* | MASA: Motif-Aware State Assignment in Noisy Time Series Data | [MASA](https://github.com/snap-stanford/masa?utm_source=catalyzex.com) |
| Ph.D. Thesis | *ProQuest '18* | Inferring Structure from Multivariate Time Series Sensor Data | None |
| Multivariate | *KDD '17* | Toeplitz Inverse Covariance-Based Clustering of Multivariate Time Series Data 🌟 | [TICC](https://github.com/davidhallac/TICC) |
| Multivariate | *KDD '17* | Network Inference via the Time-Varying Graphical Lasso 🌟 | [TVGL](https://github.com/davidhallac/TVGL) |

</div>

## [Shaghayegh Gharghabi](https://scholar.google.com/citations?hl=en&user=EITBC1YAAAAJ&view_op=list_works&sortby=pubdate) (from [Eamonn Keogh](https://www.cs.ucr.edu/~eamonn/)'s Lab, UC Riverside)

<div class="table-wrapper">

| TYPE | Venue | Paper Title and Paper Interpretation | Code |
|:---|:---|:---|:---|
| Multivariate | *DMKD '19* | Domain agnostic online semantic segmentation for multi-dimensional time series 🌟 | [Floss & datasets](https://www.cs.ucr.edu/%7eeamonn/FLOSS/) |
| Univariate | *ICDM '17* | Matrix Profile VIII Domain Agnostic Online Semantic Segmentation at Superhuman Performance Levels 🌟 | [Floss](https://sites.google.com/site/onlinesemanticsegmentation/) |

</div>

## [Shohreh Deldari](https://scholar.google.com/citations?hl=zh-CN&user=250tnREAAAAJ&view_op=list_works&sortby=pubdate) & [Flora D. Salim](https://scholar.google.com/citations?hl=zh-CN&user=Yz35RSYAAAAJ) (UNSW)

<div class="table-wrapper">

| TYPE | Venue | Paper Title and Paper Interpretation | Code |
|:---|:---|:---|:---|
| Multivariate | *JAIR '24* | Detecting Change Intervals with Isolation Distributional Kernel 🌟 | [ICD](https://github.com/IsolationKernel/Codes/tree/main/IDK/iCID) |
| Multivariate | *IMWUT '22* | COCOA Cross Modality Contrastive Learning for Sensor Data 🌟 | [COCOA](https://github.com/cruiseresearchgroup/COCOA) |
| Multivariate | *WWW '21* | Time Series Change Point Detection with Self-Supervised Contrastive Predictive Coding 🌟 | [TSCP2](https://github.com/cruiseresearchgroup/TSCP2) |
| Multivariate | *IMWUT '20* | ESPRESSO Entropy and ShaPe awaRe timE-Series SegmentatiOn for Processing Heterogeneous Sensor Data | [ESPRESSO](https://github.com/cruiseresearchgroup/ESPRESSO) |
| Multivariate | *Knowl. Inf. Syst. '20* | Unsupervised online change point detection in high-dimensional time series | None |
| Multivariate | *WSDM Workshop '19* | Inferring Work Routines and Behavior Deviations with Life-logging Sensor Data | None |
| Multivariate | *Pervasive Mob. Comput. '17* | Information gain-based metric for recognizing transitions in human activities 🌟 | [IGTs](https://github.com/cruiseresearchgroup/IGTS-python) |

</div>

## [Yasuko Matsubara](https://www.dm.sanken.osaka-u.ac.jp/~yasuko/) & [Yasushi Sakurai](https://www.dm.sanken.osaka-u.ac.jp/~yasushi/) (from [Sakurai & Matsubara Lab](https://www.dm.sanken.osaka-u.ac.jp/))

<div class="table-wrapper">

| TYPE | Venue | Paper Title and Paper Interpretation | Code |
|:---|:---|:---|:---|
| Multivariate | *KDD '24* | Mining of Switching Sparse Networks for Missing Value Imputation in Multivariate Time Series 🌟 | [MissNet](https://github.com/KoheiObata/MissNet) |
| Tensor | *WWW '24* | Dynamic Multi-Network Mining of Tensor Time Series 🌟 | [DMM](https://github.com/KoheiObata/DMM) |
| Tensor | *WWW '23* | Fast and Multi-aspect Mining of Complex Time-stamped Event Streams 🌟 | [CubeScope](https://github.com/kotaNakm/CubeScope) |
| Tensor | *KDD '22* | Fast Mining and Forecasting of Co-evolving Epidemiological Data Streams 🌟 | None |
| Tensor | *CIKM '22* | Modeling Dynamic Interactions over Tensor Streams | [Dismo](https://github.com/kokikwbt/dismo) |
| Multivariate | *CIKM '22* | Mining Reaction and Diffusion Dynamics in Social Activities 🌟 | None |
| Tensor | *NeurIPS '21* | SSMF Shifting Seasonal Matrix Factorization | [ssmf](https://github.com/kokikwbt/ssmf) |
| Tensor | *KDD '20* | Non-Linear Mining of Social Activities in Tensor Streams 🌟 | None |
| Tensor | *ICDM '19* | Multi-aspect mining of complex sensor sequences 🌟 | [CubeMarker](https://github.com/TakatoHonda/CubeMarker) |
| Multivariate | *KDD '19* | Dynamic Modeling and Forecasting of Time-evolving Data Streams | [OrbitMap](https://github.com/yasuko-matsubara/orbitmap) |
| Multivariate | *CIKM '19* | Automatic Sequential Pattern Mining in Data Streams | None |
| Multivariate | *KDD '16* | Regime Shifts in Streams: Real-time Forecasting of Co-evolving Time Sequences | [RegimeCast](https://www.dm.sanken.osaka-u.ac.jp/~yasuko/SRC/regimecast.zip) |
| Tensor | *WWW '16* | Non-linear mining of competing local activities | [CompCube](https://www.dm.sanken.osaka-u.ac.jp/~yasuko/SRC/compcube.zip) |
| Tensor | *WWW '15* | The web as a jungle: Non-linear dynamical systems for co-evolving online activities 🌟 | [Ecoweb & dataset](https://www.dm.sanken.osaka-u.ac.jp/~yasuko/SRC/ecoweb.zip) |
| Multivariate | *SIGMOD '14* | AutoPlait Automatic Mining of Co-evolving Time Sequences 🌟 | [AutoPlait](https://www.dm.sanken.osaka-u.ac.jp/~yasuko/SRC/autoplait.zip) |
| Multivariate | *ICDM '14* | Fast and Exact Monitoring of Co-evolving Data Streams | None |
| Tensor | *KDD '14* | FUNNEL Automatic Mining of Spatially Coevolving Epidemics | [Funnel](https://www.dm.sanken.osaka-u.ac.jp/~yasuko/SRC/funnel.zip) |

</div>

## Others (Selected Papers)

<div class="table-wrapper">

| TYPE | Venue | Paper Title and Paper Interpretation | Code |
|:---|:---|:---|:---|
| Multivariate | *SIGMOD '25* | ISSD: Indicator Selection for Time Series State Detection | [ISSD](https://github.com/Lab-ANT/ISSD) |
| Univariate | *OE '25* | SteadySeg Improving maritime trajectory staging by steadiness recognition | None |
| Multivariate | *AISTATS '24* | Unsupervised Change Point Detection in Multivariate Time Series | None |
| Multivariate | *WWW '24* | E2Usd: Efficient-yet-effective Unsupervised State Detection for Multivariate Time Series 🌟 | [E2Usd](https://github.com/AI4CTS/E2Usd) |
| Multivariate | *TKDE '23* | Change Point Detection in Multi-channel Time Series via a Time-invariant Representation 🌟 | [MC-TIRE](https://github.com/caozhenxiang/MC-TIRE) |
| Multivariate | *SIGMOD '23* | Time2State: An Unsupervised Framework for Inferring the Latent States in Time Series Data 🌟 | [Time2State](https://github.com/Lab-ANT/Time2State) |
| Univariate | *VLDB '24* | Raising the ClaSS of Streaming Time Series Segmentation 🌟 | [Clasp](https://github.com/ermshaua/classification-score-stream) |
| Univariate | *DMKD '23* | ClaSP: parameter-free time series segmentation 🌟 | [Clasp](https://sites.google.com/view/ts-parameter-free-clasp/) |
| Univariate | *TKDE '18* | BEATS Blocks of Eigenvalues Algorithm for Time series Segmentation 🌟 | [BEATS](https://github.com/auroragonzalez/BEATS) |
| Univariate | *Neurips '19* | U-Time: A Fully Convolutional Network for Time Series Segmentation Applied to Sleep Staging 🌟 | [U-Time](https://github.com/perslev/U-Time) |

</div>

---

**Note**: This is a condensed version of the original comprehensive paper list. The TYPE column indicates the type of time series data:
- **Univariate**: Single variable time series
- **Multivariate**: Multiple variable time series  
- **Tensor**: High-dimensional tensor time series

For the complete paper list, please visit the [original GitHub repository](https://github.com/lzz19980125/awesome-time-series-segmentation-papers). 
