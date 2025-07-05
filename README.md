# Spiking-Graph-AI-for-Anti-Money-Laundering

> **Hybrid GNN + SNN model** for detecting illicit transactions in a Bitcoin network using the [Elliptic dataset](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set).

---

## Summary

This project aims to build a **graph-based neural model** that combines:

- **Graph Neural Networks (GNN)** to learn patterns in a **cryptocurrency transaction network**
- **Spiking Neural Networks (SNN)** to capture **temporal behavior** of each transaction node using **biologically-inspired spiking mechanisms**

The goal is to detect **money laundering** and other illicit activity in a way that’s **interpretable, efficient, and time-aware**.

---

## Business Relevance

Money laundering costs the global economy billions of dollars each year. Traditional fraud detection systems struggle with:

- **Graph structure** of financial systems
- **Rapid temporal changes** in behavior
- **Low interpretability**

By combining **graph reasoning** and **temporal spiking models**, this system can better identify suspicious behavior as it emerges — especially useful in **cryptocurrency networks** where traceability is limited.

---

## Dataset: Elliptic Bitcoin Transaction Dataset

> Public dataset for anti-money laundering research in the Bitcoin blockchain.

**Key characteristics:**
- `203,769` nodes (Bitcoin transactions)
- `234,355` edges (transaction flows)
- `166` features per transaction
- `49` discrete time steps
- Labels:
  - `1` = Illicit
  - `0` = Licit
  - `-1` = Unknown (unlabeled)

[View on Kaggle](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set)

---

## Why GNN + SNN?

| Challenge                        | Solution                            |
|----------------------------------|-------------------------------------|
| Transactions are connected       | Use GNN to learn graph structure |
| Behavior evolves over time       | SNN to track timing/spikes   |
| Fraud often hides in patterns    | Combine structure + dynamics     |

This hybrid approach captures **where**, **how**, and **when** suspicious activity occurs.

---

## Project Structure

├── data/

│ └── elliptic_txs_*.csv # Raw dataset files (Kaggle)

├── src/

│ ├── preprocessing.py # Graph + feature loader

│ ├── encoder.py # Spike encoders for features/time

│ ├── model.py # GNN + SNN hybrid architecture

│ ├── train.py # Training loop
│ └── evaluate.py # Evaluation and visualization

├── notebooks/
│ └── analysis.ipynb # EDA and prototyping

├── README.md
└── requirements.txt


---

## Project Status

| Task                                          | Status   |
|-----------------------------------------------|----------|
| Load and preprocess the Elliptic dataset      | Done    |
| Build graph structure with features           | Done     |
| Encode temporal/spiking behavior              | To-Do      |
| GNN baseline classifier                       | To-Do      |
| SNN + GNN hybrid architecture                 | To-Do       |
| Model training and evaluation                 | To-Do     |
| Visualizations and interpretation             | To-Do       |
| Streamlit or web demo                         | To-Do       |

---

## Tech Stack

- [PyTorch](https://pytorch.org/) – deep learning
- [PyTorch Geometric](https://pytorch-geometric.readthedocs.io/en/latest/) – graph learning
- [SpikingJelly](https://spikingjelly.readthedocs.io/) – SNN components (or custom LIF)
- Python 3.10+
- Pandas, NumPy, NetworkX, Matplotlib

---
## Future Ideas

- Integrate attention mechanisms (GAT)
- Extend to multimodal data (e.g., device fingerprints, locations)
- Compare with traditional fraud detection models
- Export as real-time API or dashboard

## License

MIT License.
Feel free to reuse, remix, and contribute.

## Contributing

This project is in early stages — feedback, ideas, and pull requests are welcome!
If you're interested in neuromorphic computing, graph ML, or financial crime prevention, feel free to reach out.

## Author

Made by a student of ML exploring applied spiking neural networks and graph learning for business problems.





