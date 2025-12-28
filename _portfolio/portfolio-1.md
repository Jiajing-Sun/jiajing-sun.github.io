---
title: "Online Monitoring of Structural Change with Adjusted-Range Self-Normalization"
excerpt: "This paper proposes an **adjusted-range-based self-normalized sequential monitoring scheme (RSMS)** for online change-point detection, offering significant improvements in performance, especially in the presence of structural shifts. The method avoids tuning parameter choices, making it more robust and efficient for high-frequency data."
collection: portfolio
---

It connects two central themes in economic statistics: **self-normalization** and **sequential change-point detection**. **Self-normalization** provides tuning-free inference for dependent, heteroskedastic time series by avoiding long-run variance (LRV) estimation and its fragile bandwidth/kernel choices, while delivering pivotal limits under weak conditions. 

An **adjusted-range-based** self-normalizer refines classical (Shao's) self-normalization by using the **partial-sum range** rather than quadratic variation; it is less sensitive to mild contamination in the training window and grows more slowly under level shifts, thereby preserving monotonic power and robustness without extra tuning. 

**Sequential change-point detection** is crucial in real time—**when the operative question is whether today's data remain consistent with yesterday's model**—so procedures must control false alarms while signaling quickly. By combining adjusted-range self-normalization with a **CUSUM monitor**, our method offers **size-stable, tuning-free thresholds** and improved detection efficiency, yielding higher power and shorter average run lengths (ARLs) in practice.

### **Summary and Contribution**:
We develop an **online change-point detector**—RSMS, a **CUSUM-based**, **adjusted-range self-normalized monitoring scheme**—that avoids long-run variance estimation and all tuning choices (bandwidths, kernels, block lengths). We provide **finite- and open-horizon asymptotics** with ready-to-use critical values **$c_R(\alpha, d, T)$** and practical guidance on a small early-detection weight **$\gamma$**. 

Relative to quadratic (Shao's) self-normalization, the **adjusted range** curbs normalizer inflation and is more robust to mild contamination in the training window. The procedure attains **correct size** under the null hypothesis and **consistency** under the alternative hypothesis.

### **Evidence**:
Extensive simulations (VARs with homoskedastic/heteroskedastic errors and a PAR(1) count model) show that **RSMS** delivers more reliable size, higher power, and shorter ARLs than:
1. The **self-normalized scheme** of Chan et al. (2021)
2. Standard **HAC–CUSUM monitors**

In the appendix, we show that **RSMS** remains **power-stable** and continues to reduce ARLs even when the training sample is contaminated—a realistic setting because **type II errors** and **rolling re-estimation** can push shifted observations into the training window. An empirical study of functional **USD/GBP** data around the **2016 EU referendum** and **COVID-19** shows that **RSMS** flags major breaks promptly, often earlier than alternatives and frequently with the shortest ARL.

### **R Code and Full Paper**:
You can access the **R code** at [Zenodo](https://doi.org/10.5281/zenodo.17460569), and the **full paper** is available at [Manuscript](https://jiajing-sun.github.io/files/ASN_sequential.pdf).
