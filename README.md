# 🧠 Deep Learning in Finance 

This repository contains the practical work (TPs) completed as part of the **Deep Learning in Finance** course at CentraleSupélec. Each lab addresses a specific topic in financial modeling using deep learning, ranging from estimation of Hurst exponents to GANs and autoencoders for financial time series.

---

### 📁 Structure

```bash
.
├── TP1_estimation/         # Hurst exponent estimation with DNNs and CNNs
├── TP2_options/            # Option pricing with deep networks
├── TP3_GAN/                # Basic GANs for financial time series
├── TP4_GAN_bis/            # Advanced GANs (Relativistic, condGAN, CorrGAN)
├── TP5_AE/                 # Autoencoders for market states & anomaly detection
├── TP6_prediction/         # LSTM-based return prediction
└── README.md
```

---

## 🔧 Setup

All notebooks are written in Python using `TensorFlow`, `Keras`, `Pandas`, `NumPy`, and `Matplotlib`.

Install the dependencies with:

```bash
pip install -r requirements.txt
```

*(Note: you may need to create this file based on your notebook's `import` statements.)*

---

## 🧪 Project Overview

### **TP1 – Estimation of the Hurst Exponent**

* Estimate Hurst exponent $H$ and volatility from fractional Brownian motion using:

  * Dense Neural Networks (DNN)
  * 1D and 2D Convolutional Neural Networks (CNNs)
* Optional: hyperparameter optimization with **Talos**
* Evaluate bias and MAE of predictions by value of $H$

> 📎 *Topic: Time series generation, regression, scaling, CNN architectures*

---

### **TP2 – Option Pricing**

* Predict the mid-price of options using increasingly informative features:

  1. Strike/mid, time to maturity, spread
  2. * Volatility estimate (e.g., Rogers-Satchell)
  3. * Black-Scholes theoretical price
  4. * Put-call parity constraints with custom loss functions

> 📎 *Topic: Regression with domain knowledge, model constraints, custom loss*

---

### **TP3 – Generative Adversarial Networks (Intro)**

* First implementation of GANs on financial returns
* Explore:

  * Dense Generator and Discriminator architectures
  * Stylized facts: fat tails, autocorrelation of returns and absolute returns

> 📎 *Topic: Basic GANs, time series generation, stylized financial metrics*

---

### **TP4 – Advanced GAN Architectures**

Choose among:

1. **Relativistic GANs** with stylized loss terms
2. **Conditional GANs** using financial context
3. **CorrGANs** for generating correlation matrices

Each model is evaluated on its ability to reproduce realistic financial behaviors.

> 📎 *Topic: GAN tuning, conditional generation, correlation modeling*

---

### **TP5 – Autoencoders**

* Build autoencoders to:

  1. Cluster **assets** based on return patterns
  2. Cluster **days** to identify market regimes
  3. Detect **anomalies** based on reconstruction error

> 📎 *Topic: Dimensionality reduction, latent space interpretation, unsupervised learning*

---

### **TP6 – Return Prediction with LSTM**

* Predict future returns using:

  1. Past returns (1/5/22 days)
  2. * Technical indicators (MACD, etc.)
  3. * Optional custom features (e.g., Hurst, AE encodings)

Compare model performance with/without dropout and multiple feature sets.

> 📎 *Topic: Sequence modeling, sliding window training, LSTM evaluation*

---

## 📊 Key Themes

* Time Series Regression & Generation
* Stylized Financial Metrics
* CNNs, LSTMs, Autoencoders, GANs
* Volatility Estimation & Option Pricing
* Custom Losses and Domain Constraints

---

## 📚 References

* [fbm](https://pypi.org/project/fbm/) for fractional Brownian motion
* [Talos](https://github.com/autonomio/talos) for hyperparameter tuning
* Stone, H. (2020) "Financial Time Series with CNNs"
* Koshiyama et al. (2020) for conditional GANs
* Marti et al. (2020) for correlation modeling

---

## 🧑‍🎓 Author

This project was developed as part of a **university course on Deep Learning in Finance**, during the Fall 2024 semester.