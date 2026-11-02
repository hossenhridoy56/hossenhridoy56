<div align="center">

# 👨‍🔬 MD. HRIDOY HOSSEN
### **Academic Researcher & Statistician**
**Department of Statistics & Data Science, Islamic University, Kushtia, Bangladesh**

[![M.Sc. in Statistics](https://img.shields.io/badge/M.Sc._in_Statistics-In_Progress_(Exp._2027)-1E3A8A?style=for-the-badge&logo=academia&logoColor=white)](#-academic-background--credentials)
[![B.Sc. in Statistics](https://img.shields.io/badge/B.Sc._in_Statistics-CGPA_3.46_%2F_4.00-0284C7?style=for-the-badge)](#-academic-background--credentials)
[![IELTS Academic](https://img.shields.io/badge/IELTS_Academic-Band_7.0_(C1)-059669?style=for-the-badge)](#-academic-background--credentials)

<br/>

[![MVT Zenodo DOI](https://img.shields.io/badge/MVT_DOI-10.5281%2Fzenodo.22861296-0057B7?style=flat&logo=zenodo&logoColor=white)](https://doi.org/10.5281/zenodo.22861296)
[![Climate Zenodo DOI](https://img.shields.io/badge/Climate_DOI-10.5281%2Fzenodo.23324622-0057B7?style=flat&logo=zenodo&logoColor=white)](https://doi.org/10.5281/zenodo.23324622)
[![Academic Email](https://img.shields.io/badge/Institutional_Email-hridoy1922025.stat%40std.iu.ac.bd-C5221F?style=flat&logo=gmail&logoColor=white)](mailto:hridoy1922025.stat@std.iu.ac.bd)
[![Personal Email](https://img.shields.io/badge/Personal_Email-hossenhridoy56%40gmail.com-D14836?style=flat&logo=mail.ru&logoColor=white)](mailto:hossenhridoy56@gmail.com)
[![Stratosphere Live](https://img.shields.io/badge/Live_System-Stratosphere_Gateway-4B32C3?style=flat&logo=render&logoColor=white)](https://stratosphere-gateway.onrender.com/)

</div>

---

## 📌 Executive Summary
Statistics graduate and researcher specializing in **Functional Data Analysis (FDA)**, **Time Series Econometrics & Asymptotics**, and **Hydro-Climatological Statistical Modeling**. Currently serving as a **Research Assistant** on a UGC-funded national climate project and completing thesis research for an M.Sc. in Statistics at Islamic University, Kushtia. Passionate about formulating likelihood-based finite mixture models, developing noncentral asymptotic derivations, conducting high-throughput Monte Carlo experiments, and deploying reproducible computational architectures.

---

## 🌟 Flagship Research: Functional Data Analysis (FDA)

### 📈 M.Sc. Thesis Project
> ### **"Model-Based Clustering of Climatological Functional Data with Temporal Dependence: An Autoregressive Mixture Model for Bangladesh Monsoon Rainfall"**
> *Supervised by Md. Matiur Rahman Molla, Associate Professor, Department of Statistics & Data Science, Islamic University, Kushtia*

* **Research Motivation:** Standard functional clustering models assume that curve observations across repeated years are mutually independent given cluster membership. In multi-decadal climatology, annual rainfall trajectories exhibit noticeable serial persistence. Ignoring this dependence causes severe over-clustering in standard Bayesian Information Criterion (BIC) selection.
* **Methodological Framework:**
  - **Representation:** Curves $Y_{i,t}(s)$ transformed into $d$-dimensional score vectors $\boldsymbol{\xi}_{i,t} \in \mathbb{R}^d$ via pooled Functional Principal Component Analysis (FPCA).
  - **Dynamic Latent Scores:** Scores follow a stationary Gaussian vector AR(1) process around cluster means:
    $$\boldsymbol{\xi}_{i,t} = \boldsymbol{\mu}_g + \boldsymbol{u}_{i,t}, \quad \boldsymbol{u}_{i,t} = \phi \boldsymbol{u}_{i,t-1} + \boldsymbol{\epsilon}_{i,t}, \quad |\phi| < 1, \quad \boldsymbol{\epsilon}_{i,t} \sim \mathcal{N}_d(\mathbf{0}, \boldsymbol{\Sigma}_g)$$
  - **Exact Likelihood Derivation:** Utilizing a **Prais–Winsten transformation** with lower-triangular Jacobian determinant $(1-\phi^2)^{d/2}$ preserving observed-data likelihood:
    $$\mathcal{L}(\boldsymbol{\Theta}) = \prod_{i=1}^N \left[ (1 - \phi^2)^{d/2} \sum_{g=1}^G \pi_g \prod_{t=1}^T f_d\left(\tilde{\boldsymbol{\xi}}_{i,t};\, a_t(\phi)\boldsymbol{\mu}_g,\, \boldsymbol{\Sigma}_g\right) \right]$$
* **Estimation & Diagnostics:** Generalized Expectation-Maximization (EM) algorithm with bounded one-dimensional optimization for $\phi$, likelihood decrease safeguards, model selection via BIC and ICL with effective sample size adjustments $T_{\text{eff}} \approx T\frac{1-\phi}{1+\phi}$.
* **Empirical Testbed:** 76 years (1950–2025) of continuous ERA5-Land daily precipitation records across Bangladesh.

---

## 🔬 Core Research Domains & Scholarly Contributions

### 1. 📉 Time Series Econometrics & Asymptotic Distribution Theory
#### **A Novel Massive Variance Stability Test: Theory, Distributional Derivations, and Superior Performance Under Structural Breaks**
[![DOI](https://img.shields.io/badge/Zenodo_DOI-10.5281%2Fzenodo.22861296-0057B7?style=flat&logo=zenodo&logoColor=white)](https://doi.org/10.5281/zenodo.22861296)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/hossenhridoy56/massive-variance-stability-test/blob/main/LICENSE)
[![Software Heritage](https://img.shields.io/badge/Software_Heritage-Archived-blue)](https://archive.softwareheritage.org/swh:1:dir:fb0bcdf3cc816ccb214bf4da7c67ec3bba458077)

* **Mathematical Formulation:** Designed a global test statistic ($Q_{\mathrm{MVT}}$) for variance stationarity across partitioned non-overlapping segments of size $m = n/k$:
  $$Q_{\mathrm{MVT}} = \frac{m-1}{2\bar{v}^2} \sum_{j=1}^k (v_j - \bar{v})^2 \overset{d}{\longrightarrow} \chi^2_{k-1}$$
* **Theoretical Derivations:** Derived finite-sample representations and noncentral chi-square formulations under sudden parameter shifts at segment boundaries.
* **Large-Scale Simulation:** Executed 10,000 Monte Carlo replications evaluating empirical size distortion, non-Gaussian innovations, ARCH-type conditional heteroskedasticity, and comparative statistical power against Bartlett, Levene, Goldfeld–Quandt, Breusch–Pagan, White, and ICSS procedures.
* **Empirical Analysis:** Evaluated 4,997 daily Gold Futures price observations (2005–2026), demonstrating severe structural volatility transitions ($p \approx 7.67 \times 10^{-258}$).
* 🔗 **Repository:** [massive-variance-stability-test](https://github.com/hossenhridoy56/massive-variance-stability-test)

---

### 2. 🌦️ Climatological Reclassification & Machine Learning Clustering (UGC Funded)
#### **A Cluster Analysis of Bangladesh's Monthly Climate and Its Comparison with the Traditional Six-Season Calendar**
[![Peer Review](https://img.shields.io/badge/Status-Under_Review-orange?style=flat)](https://github.com/hossenhridoy56/Bangladesh-Seasonal-Reclassification)
[![Journal](https://img.shields.io/badge/Journal-Theoretical_and_Applied_Climatology-blue?style=flat)](https://github.com/hossenhridoy56/Bangladesh-Seasonal-Reclassification)
[![DOI](https://img.shields.io/badge/Zenodo_DOI-10.5281%2Fzenodo.23324622-0057B7?style=flat&logo=zenodo&logoColor=white)](https://doi.org/10.5281/zenodo.23324622)

* **Institutional Project:** UGC-Funded Research Project (Fiscal Year 2025–2026) | *Supervisor: Md. Matiur Rahman Molla*
* **Observational Dataset:** 30 years (1985–2014) of verified ground observations spanning **10,865 station-months** across 33 BMD weather stations in a 6-variable climate space ($T_{\max}, T_{\min}$, rainfall, humidity, wind speed, cloud cover).
* **Algorithmic Suite:** Comparative application of K-Means, DBSCAN, and Hierarchical Agglomerative Clustering along with PCA dimensionality reduction and Dynamic Time Warping (DTW).
* **Scientific Discovery:** Uncovered definitive empirical evidence establishing a modern 4-season climatological structure (Winter, Pre-Monsoon, Monsoon, Post-Monsoon) with October serving as an independent transition month, critically challenging the traditional literary 6-season paradigm.
* 🔗 **Repository:** [Bangladesh-Seasonal-Reclassification](https://github.com/hossenhridoy56/Bangladesh-Seasonal-Reclassification)

---

### 3. 🌊 Hydro-Climatic Dynamics & Bayesian Time-Series Modeling
#### **Resolving Monsoon Timing Shifts in Bangladesh (1981–2025): Observational Uncertainty & Finite-Sample Detection**
[![Data: ERA5 & CHIRPS](https://img.shields.io/badge/Data-ERA5--Land_%26_CHIRPS_(45_Yrs)-green)](https://github.com/hossenhridoy56)
[![Modeling](https://img.shields.io/badge/Modeling-Autoregressive_Bayesian-purple)](https://github.com/hossenhridoy56)

* **Multi-Decadal Ingestion:** Integrated 45 years of gridded daily precipitation reanalysis and satellite products.
* **Trend & Teleconnection Detection:** Developed non-parametric rainfall-based indices for monsoon onset, peak, and withdrawal; applied Mann-Kendall trend tests with False Discovery Rate (FDR) control and Bayesian autoregressive time-series models capturing ENSO-driven variability.
* **Uncertainty Quantification:** Deployed extensive Monte Carlo experiments to evaluate finite-sample detection thresholds and observational uncertainty in regional hydro-meteorology.

---

### 4. 🏥 Environmental Epidemiology & Climate-Health Vulnerability
#### **Climate-Health Vulnerability Assessment in Bangladesh: A Spatial Data-Driven Statistical Framework**
[![Districts](https://img.shields.io/badge/Spatial_Coverage-64_Districts_of_Bangladesh-teal)](https://github.com/hossenhridoy56)
[![Survey: MICS 2025](https://img.shields.io/badge/Survey_Data-MICS_2025-red)](https://github.com/hossenhridoy56)

* **Cross-Disciplinary Synthesis:** Merged 30 years (1995–2024) of ERA5-Land climate reanalysis with nationwide MICS 2025 public health, demographic, and socioeconomic indicators.
* **Multivariate Dimensionality Reduction:** Executed Principal Component Analysis (PCA) over seven core climate indicators, isolating three principal components that account for **89.73% of total variance**.
* **Composite Index Construction:** Derived standardized indices for Climate Exposure, Health Sensitivity, Adaptive Capacity, and Disaster Exposure, mapping critical spatial vulnerability hotspots in coastal and hill-tract districts (Bhola, Patuakhali, Bandarban, Rangamati, Cox's Bazar).

---

### 5. 💻 Computational Infrastructure & Scientific Web Platforms
#### **Stratosphere Gateway: Intelligent Departmental Management System with Generative AI**
[![Live App](https://img.shields.io/badge/Status-Live_Production-success?style=flat&logo=render&logoColor=white)](https://stratosphere-gateway.onrender.com/)
[![Locust Tested](https://img.shields.io/badge/Load_Testing-24.4_RPS_%7C_0%25_Failure-blue)](https://github.com/hossenhridoy56/stratosphere-gateway)

* **Architecture:** Full-stack departmental computational gateway built on Python (Flask), SQLAlchemy, PostgreSQL, and Bootstrap.
* **Generative Automation:** Deployed Generative AI-assisted pipelines for automated generation and verification of academic transcripts, certificates, and student attendance analytics.
* **Stress Tested:** Validated via Locust performance profiling, demonstrating high concurrency resilience (24.4 Requests/sec, 0% failure rate under sustained load).
* 🔗 **Repository:** [stratosphere-gateway](https://github.com/hossenhridoy56/stratosphere-gateway)

---

## 🛠️ Methodological & Technical Ecosystem

| Research Discipline | Methodologies & Theoretical Frameworks | Computational Tools & Libraries |
| :--- | :--- | :--- |
| **Functional Data Analysis (FDA)** | FPCA score reduction, Prais–Winsten transformed AR(1) mixtures, Generalized EM, BIC/ICL criteria | `Python (scikit-learn, SciPy)`, `R (fda, funData)` |
| **Statistical Inference & Econometrics** | MVT variance stability test, asymptotic distribution derivations, Monte Carlo simulations | `Python (NumPy, statsmodels)`, `R (tidyverse, ggplot2)` |
| **Hydro-Climatology & Spatial Analysis** | Grid-based reanalysis handling, Mann-Kendall trend detection, composite PCA index synthesis | `Xarray`, `Pandas`, `Matplotlib`, `Seaborn`, `ERA5-Land` |
| **Statistical Packages & Legacy Tools** | Survey data processing, linear regression, biostatistics, survey sampling | `SPSS`, `STATA`, `SAS`, `SQL (PostgreSQL)` |
| **Engineering & Scientific Publishing** | High-concurrency web gateways, automated reporting, version control, technical typesetting | `Flask`, `SQLAlchemy`, `LaTeX`, `Overleaf`, `BibTeX`, `Git` |

---

## 🎓 Academic Background & Credentials

- **Master of Science (M.Sc.) in Statistics (In Progress)**  
  *Department of Statistics & Data Science, Islamic University, Kushtia, Bangladesh*  
  *Duration:* Currently enrolled (Expected Completion: March 2027)  
  *Thesis:* *Model-Based Clustering of Climatological Functional Data with Temporal Dependence: An Autoregressive Mixture Model for Bangladesh Monsoon Rainfall*

- **Bachelor of Science (B.Sc.) in Statistics**  
  *Department of Statistics & Data Science, Islamic University, Kushtia, Bangladesh*  
  *Duration:* Dec 2019 – Nov 2025 | **CGPA: 3.46 / 4.00** (160 Credits completed)  
  *Core Coursework:* Statistical Inference, Regression Analysis, Time Series Analysis, Probability & Measure, Bayesian & Classical Inference, Matrix Algebra, Sampling Techniques, Multivariate Analysis, Stochastic Processes.

- **Language Proficiency:**  
  *IELTS Academic:* **Overall Band 7.0 (CEFR Level C1)**  
  *(Listening: C1, Reading: C1, Speaking: B2, Writing: B2)*

---

## 📊 Research Activity & Computational Metrics

<div align="center">
  <img src="https://github-readme-stats-fast.vercel.app/api?username=hossenhridoy56&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="Hridoy's GitHub Stats" height="165"/>
  <img src="https://github-readme-stats-fast.vercel.app/api/top-langs?username=hossenhridoy56&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" height="165"/>
</div>

<div align="center" style="margin-top: 10px;">
  <img src="https://streak-stats.demolab.com/?user=hossenhridoy56&theme=tokyonight&hide_border=true" alt="GitHub Streak" height="165"/>
</div>

---

## 📬 Contact & Research Opportunities
I actively welcome collaborative research projects, pre-doctoral/PhD fellowship inquiries, and academic discussions in Functional Data Analysis, Time Series Econometrics, and Climate Statistics.

- 🏢 **Academic Office:** Department of Statistics & Data Science, Islamic University, Kushtia-7003, Bangladesh
- ✉️ **Institutional Email:** [hridoy1922025.stat@std.iu.ac.bd](mailto:hridoy1922025.stat@std.iu.ac.bd)
- ✉️ **Personal Email:** [hossenhridoy56@gmail.com](mailto:hossenhridoy56@gmail.com)
- 🌐 **Academic Codebase:** [github.com/hossenhridoy56](https://github.com/hossenhridoy56)
- 📦 **Zenodo Author Archive:** [Zenodo / hossenhridoy56](https://zenodo.org/search?q=metadata.creators.person_or_org.name:%22hossenhridoy56%22)
