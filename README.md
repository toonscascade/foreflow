# References — Foreflow: A World-Model Approach to Predictive Cyber Defence
### SIH26153 — AI-Based Network Attack Forecasting from Network Traffic Data

---

## 1. Core Concept — World Models

**Ha, D., & Schmidhuber, J. (2018). World Models.**
arXiv:1803.10122
🔗 https://arxiv.org/abs/1803.10122

> Introduced the concept of learning a compressed, unsupervised internal simulation of an environment's dynamics — enabling prediction of future states rather than reactive classification. Foundational concept our forecasting engine is built on.

**Ha, D., & Schmidhuber, J. (2018). Recurrent World Models Facilitate Policy Evolution.**
arXiv:1809.01999
🔗 https://arxiv.org/abs/1809.01999

---

## 2. Dataset

**Sharafaldin, I., Lashkari, A. H., & Ghorbani, A. A. (2018). Toward Generating a New Intrusion Detection Dataset and Intrusion Traffic Characterization.**
Proceedings of the 4th International Conference on Information Systems Security and Privacy (ICISSP), pp. 108–116.
🔗 https://www.scitepress.org/papers/2018/66398/66398.pdf

**CSE-CIC-IDS2018 Dataset — Canadian Institute for Cybersecurity, University of New Brunswick**
🔗 https://www.unb.ca/cic/datasets/ids-2018.html
> 80+ labeled network traffic features, 7 attack types (Brute-force, Heartbleed, Botnet, DoS, DDoS, Web attacks, Infiltration). AWS-hosted, publicly redistributable with citation.

**CTU-13 Dataset — Garcia, S., Grill, M., Stiborek, J., & Zunino, A. (2014). An Empirical Comparison of Botnet Detection Methods.**
Computers & Security, 45, 100–123.
🔗 https://www.stratosphereips.org/datasets-ctu13
> Real botnet traffic captures mixed with normal and background traffic — alternative/supplementary dataset option named in the official PS.

---

## 3. Model Architecture

**Lo, W. W., Layeghy, S., Sarhan, M., Gallagher, M., & Portmann, M. (2022). E-GraphSAGE: A Graph Neural Network based Intrusion Detection System for IoT.**
IEEE/IFIP Network Operations and Management Symposium (NOMS) 2022.
🔗 https://arxiv.org/abs/2103.16329

> Demonstrated that representing network flows as a graph (nodes = hosts, edges = flow features) and applying GNNs outperforms traditional flow-based classifiers across 4 benchmark datasets.

**Bilot, T., et al. Graph Neural Networks for Intrusion Detection: A Survey.**
🔗 https://www.researchgate.net/publication/370733865_Graph_Neural_Networks_for_Intrusion_Detection_A_Survey

---

## 4. Explainability

**Lundberg, S. M., & Lee, S.-I. (2017). A Unified Approach to Interpreting Model Predictions.**
Advances in Neural Information Processing Systems 30 (NeurIPS 2017).
🔗 https://arxiv.org/abs/1705.07874

> Introduced SHAP (SHapley Additive exPlanations) — the mathematically grounded feature-attribution framework (19,000+ citations) our explainability layer is built on. Directly satisfies the PS requirement that "black-box outputs are not acceptable."

---

## 5. Attack Taxonomy

**MITRE ATT&CK Framework — MITRE Corporation (released 2013).**
🔗 https://attack.mitre.org

> Industry-standard, publicly maintained knowledge base of adversary tactics and techniques based on real-world observations. 300+ documented techniques across 14 tactics (Reconnaissance, Initial Access, Execution, Persistence, Lateral Movement, Command & Control, Exfiltration, etc.). Formally recognized by CISA for threat intelligence standardization.

---

## 6. Industry Impact Data

**IBM Security. (2025). Cost of a Data Breach Report 2025.**
IBM Security & Ponemon Institute.
🔗 https://www.ibm.com/reports/data-breach

> Global average breach lifecycle: 241 days (181 to identify + 60 to contain). Breaches contained under 200 days cost $3.87M vs. $5.01M for longer — a $1.14M premium for slow detection. Organizations using AI security tools extensively cut breach lifecycle by 80 days and saved ~$1.9M on average.

---

## 7. Tools & Frameworks Used in Implementation

| Tool | Purpose | Link |
|---|---|---|
| PyTorch | Core deep learning framework (LSTM/Transformer world model) | https://pytorch.org |
| PyTorch Geometric (PyG) | Graph Neural Network implementation | https://pytorch-geometric.readthedocs.io |
| scikit-learn | Baseline logistic regression model, evaluation metrics (F1, precision, recall) | https://scikit-learn.org |
| SHAP (library) | Feature attribution / explainability implementation | https://github.com/shap/shap |
| Captum | PyTorch-native attention/interpretability extraction | https://captum.ai |
| Scapy | Packet-level PCAP parsing | https://scapy.net |
| PyShark | Wireshark-based PCAP parsing (tshark wrapper) | https://github.com/KimiNewt/pyshark |
| CICFlowMeter | Flow-level feature extraction from raw packets | https://www.unb.ca/cic/research/applications.html |
| Streamlit | Offline demonstration interface | https://streamlit.io |
| attackcti | Python library for querying MITRE ATT&CK STIX/TAXII data | https://github.com/OTRF/attackcti |

---

## 8. Blockchain Trust Layer Extension (Problems 5–8, team-designed addition)

| Tool | Purpose | Link |
|---|---|---|
| Hyperledger Fabric | Permissioned blockchain for multi-org threat intel sharing | https://www.hyperledger.org/projects/fabric |
| Ganache | Local Ethereum blockchain for demo/testing | https://trufflesuite.com/ganache |
| IPFS | Off-chain storage for evidence bundles | https://ipfs.tech |

---

*Compiled for SIH 2026 — PS SIH26153 (AI-Based Network Attack Forecasting from Network Traffic Data). All sources are publicly available and independently verifiable.*
