# 🌐 Federated Learning Simulation for Privacy-Preserving Healthcare Prediction

A complete implementation of a **Federated Learning (FL)** simulation using the **Flower Framework** and **Scikit-learn**. The project demonstrates how multiple healthcare institutions collaboratively train a global machine learning model without exchanging sensitive patient data, preserving privacy while enabling collaborative learning.

---

# 📌 Project Overview

Traditional centralized machine learning requires collecting all data into a single location, creating privacy, security, and regulatory challenges—especially in healthcare.

This project simulates a federated learning environment where multiple healthcare clients independently train a **Logistic Regression** model on their local datasets. Instead of sharing patient records, only model parameters are transmitted to a central server for aggregation using the **Federated Averaging (FedAvg)** algorithm.

The notebook covers the entire federated learning workflow, including client-side training, server aggregation, global model evaluation, and feature importance analysis.

---

# ✨ Features

- 🔒 Privacy-preserving distributed learning
- 🏥 Simulation of multiple healthcare clients
- 🌐 Flower Federated Learning framework
- 🧠 Logistic Regression classifier
- 📊 Federated Averaging (FedAvg)
- 📈 Global model evaluation
- 📉 Precision, Recall, F1-Score, ROC-AUC analysis
- 📊 Confusion Matrix visualization
- 📋 Feature importance analysis
- 📉 Client-wise performance comparison
- 📈 Loss visualization
- 🔍 ROC Curve generation

---

# 🏗️ System Architecture

```
          Client P
              │
          Local Training
              │
              ▼
          Model Weights
              │
              │
Client L ─────────────►
              │
Client H ─────────────►     Flower Server
              │          (FedAvg Aggregation)
Client Br────────────►
              │
              ▼
      Global Model Update
              │
              ▼
     Broadcast Updated Model
```

Each client trains on its own private dataset.

Only model parameters are exchanged.

Raw data never leaves the local machine.

---

# 🚀 Workflow

1. Load distributed client datasets
2. Initialize Flower server
3. Create federated clients
4. Train local Logistic Regression models
5. Aggregate parameters using FedAvg
6. Update the global model
7. Repeat for multiple communication rounds
8. Evaluate the global model
9. Analyze feature importance
10. Visualize results

---

# 🧠 Machine Learning Model

**Algorithm**

- Logistic Regression

**Solver**

- liblinear

**Task**

- Binary Classification

The choice of Logistic Regression provides:

- High interpretability
- Fast convergence
- Lightweight communication
- Efficient federated updates

---

# 🔒 Privacy-Preserving Learning

Unlike centralized learning:

❌ Raw patient records are never shared.

✅ Only learned model coefficients are transmitted to the central server.

This architecture aligns with modern privacy-preserving AI principles and is suitable for sensitive domains such as healthcare.

---

# 🛠 Technologies Used

- Python
- Flower (FLWR)
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- Seaborn

---

# 📁 Project Structure

```
.
├── Fedrated_Learning_Simulation.ipynb
├── Federated_Learning_Simulation.pdf
├── client_data/
│   ├── client_P.xlsx
│   ├── client_L.xlsx
│   ├── client_H.xlsx
│   └── client_Br.xlsx
├── outputs/
│   ├── plots/
│   └── metrics/
└── README.md
```

---

# 📊 Performance Metrics

The notebook evaluates the federated model using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- Weighted Loss

The accompanying report shows the trained global model achieved:

| Metric | Result |
|---------|---------|
| Accuracy | **74.44%** |
| Precision | **74.71%** |
| Recall | **98.48%** |
| F1 Score | **0.8497** |
| ROC-AUC | **0.6155** |
| Weighted Loss | **0.5604** |

These results indicate excellent sensitivity for positive cases while highlighting opportunities to improve specificity and reduce false positives. :contentReference[oaicite:0]{index=0}

---

# 📈 Visualizations

The project includes visualizations for:

- Precision vs Recall
- Client-wise Loss
- ROC Curve
- Confusion Matrix
- Feature Importance Rankings
- Performance Metrics Comparison

---

# 📊 Feature Importance

The notebook analyzes model coefficients to identify which clinical features contribute most strongly to predictions across different healthcare clients.

Since every institution has different local data distributions, feature importance varies among clients, demonstrating the heterogeneous nature of federated learning. :contentReference[oaicite:1]{index=1}

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Federated-Learning-Simulation.git
```

Navigate to the project:

```bash
cd Federated-Learning-Simulation
```

Install dependencies:

```bash
pip install flwr
pip install scikit-learn
pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn
pip install openpyxl
```

---

# ▶️ Run the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
Fedrated_Learning_Simulation.ipynb
```

Run all cells to:

- Simulate federated clients
- Train local models
- Aggregate model parameters
- Evaluate the global model
- Generate performance visualizations

---

# 🎯 Learning Outcomes

This project demonstrates:

- Federated Learning Fundamentals
- Distributed Machine Learning
- Flower Framework
- Privacy-Preserving AI
- Healthcare AI Applications
- Logistic Regression
- FedAvg Aggregation
- Model Evaluation
- Explainable Machine Learning
- Collaborative Learning Systems

---

# 🔮 Future Improvements

Potential enhancements include:

- Differential Privacy
- Secure Aggregation
- Federated Neural Networks
- Personalized Federated Learning
- Non-IID Data Handling
- Adaptive Federated Optimization (FedProx, FedAdam)
- Cross-Silo Federated Learning
- Real-Time Client Participation
- Model Compression for Communication Efficiency
- Homomorphic Encryption Integration

---

# 👨‍💻 Author

**Muhammad Hassan Tahir**

AI Engineer | Machine Learning | Federated Learning | Computer Vision | Deep Learning

---

# 📜 License

This project is intended for educational, research, and demonstration purposes.
