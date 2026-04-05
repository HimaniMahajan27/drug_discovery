<div align="center">

# 🧠 UXGNN — Unified Explainable Graph Neural Network

### 🚀 Drug Discovery using Explainable Graph Neural Networks

<img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" width="150"/>

<br/>

<img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/PyTorch-red?style=for-the-badge"/>
<img src="https://img.shields.io/badge/PyG-purple?style=for-the-badge"/>
<img src="https://img.shields.io/badge/XAI-green?style=for-the-badge"/>

</div>

---

## 📌 Overview

UXGNN is a **Graph Neural Network framework** for **molecular property prediction in drug discovery**.

* 🧪 Molecules → Graphs
* ⚙️ Edge-aware message passing
* 🎯 Attention pooling
* 🔍 Explainability integrated

---

## 🔄 Model Pipeline

```
🧪 Raw Molecule
        ↓
🕸️ Graph Construction
        ↓
⚙️ Edge-Aware Message Passing
        ↓
🎯 Attention Pooling
        ↓
🔗 Multi-Scale Readout
        ↓
📊 Prediction + Explainability
```

---

## 🏗️ Key Innovations

| Feature                   | Description                 | Benefit                    |
| :------------------------ | :-------------------------- | :------------------------- |
| ⚙️ Edge-Aware Convolution | Uses bond information       | Better relational learning |
| 🎯 Attention Pooling      | Learns important atoms      | Improved interpretability  |
| 🔗 Multi-Scale Readout    | Combines pooling strategies | Richer representation      |

---

## 📊 Datasets

| Dataset | Details                           | Type       |
| :------ | :-------------------------------- | :--------- |
| BBBP    | ~2,000 molecules · 77% positive   | Binary     |
| HIV     | ~40,000 molecules · 3.5% positive | Binary     |
| Tox21   | ~8,000 molecules · 8% positive    | Multi-task |

---

## 📈 Prediction Performance

| Dataset | Model |     AUC    |  Accuracy  |     F1     |  Time |
| :------ | :---- | :--------: | :--------: | :--------: | :---: |
| BBBP    | GCN   |   0.9297   |   0.8195   |   0.8737   |  0.5m |
| BBBP    | GAT   |   0.9002   |   0.8098   |   0.8651   |  0.5m |
| BBBP    | GIN   | **0.9382** | **0.8488** | **0.8942** |  0.4m |
| BBBP    | UXGNN |   0.9354   |   0.8341   |   0.8836   |  0.4m |
| HIV     | GCN   | **0.8036** |   0.9545   |   0.4384   |  5.6m |
| HIV     | GAT   |   0.7930   |   0.9536   |   0.4050   | 12.8m |
| HIV     | GIN   |   0.8016   | **0.9647** |   0.5183   | 11.7m |
| HIV     | UXGNN |   0.7774   |   0.9210   |   0.3590   |  8.2m |
| Tox21   | GCN   |   0.7951   | **0.9615** |   0.5333   |  1.1m |
| Tox21   | GAT   | **0.7983** |   0.8666   |   0.2707   |  0.7m |
| Tox21   | GIN   |   0.7581   |   0.9560   |   0.5294   |  0.5m |
| Tox21   | UXGNN |   0.7933   |   0.9106   | **0.5862** |  0.9m |

---

## 🔍 Explainability

| Method               |  Fidelity |  Sparsity | Stability |
| :------------------- | :-------: | :-------: | :-------: |
| Attention (UXGNN)    |   0.125   |   0.400   | **0.997** |
| Integrated Gradients |   0.149   |   0.611   |   0.994   |
| GNNExplainer         |   0.176   |   0.360   |   0.856   |
| GraphSHAP            | **0.354** | **0.786** |   0.983   |

> Attention = highest stability
> GraphSHAP = best fidelity + sparsity

---

## 🧪 Ablation Study

| Variant              |     AUC    |     ΔAUC    |
| :------------------- | :--------: | :---------: |
| Full UXGNN           | **0.9354** |    0.0000   |
| w/o Edge             |   0.9309   |   -0.0045   |
| w/o Attention        |   0.9277   |   -0.0077   |
| w/o Multi-scale      |   0.9305   |   -0.0050   |
| w/o Edge + Attention |   0.9263   | **-0.0092** |

---

## 💪 Robustness

| Noise | Consistency |
| :---: | :---------: |
|  0.00 |     100%    |
|  0.01 |    98.7%    |
|  0.05 |    96.5%    |
|  0.10 |    94.8%    |

---

## 🚀 How to Run

```bash
git clone <repo_url>
cd UXGNN
pip install -r requirements.txt
python train.py
```

---

## 🤝 Contributing

* Fork repo
* Create branch
* Submit PR

---

## ⭐ Conclusion

✔ Strong prediction
✔ Explainability
✔ Robust performance

---

## 🙌 Author

**Himani Mahajan 🌷**
