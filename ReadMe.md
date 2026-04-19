
# 🧠 Self-Pruning Neural Network (Automatic Model Compression)

A **PyTorch-based Self-Pruning Neural Network** that **learns to remove unnecessary weights automatically during training** using learnable gates and sparsity regularization.

This project demonstrates **model compression, efficient AI, and research-style experimentation** using CIFAR-10.

---

# 🚀 Features

* ✅ Learnable Gate-Based Pruning
* ✅ Automatic Weight Reduction
* ✅ Sparsity Regularization (L1)
* ✅ CIFAR-10 Training Pipeline
* ✅ Pretrained Model Support
* ✅ Resume Training
* ✅ Accuracy vs Sparsity Experiments
* ✅ Gate Distribution Visualization
* ✅ Clean Modular Codebase

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/niha1905/Tredence-Analytics-AI-Engineering-case-study.git

```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# 📊 Dataset

This project uses **CIFAR-10** dataset:

* 60,000 images
* 10 classes
* 32x32 RGB images

Dataset downloads automatically during training.

---

# 🧠 Model Architecture

Self-Pruning Network:

```
Input (32x32x3)
        ↓
Prunable Linear (512)
        ↓
ReLU
        ↓
Prunable Linear (256)
        ↓
ReLU
        ↓
Prunable Linear (10)
        ↓
Output
```

Each layer contains:

* Learnable weights
* Learnable gates
* Automatic pruning

---

# 🔧 How It Works

Each weight has a **learnable gate**

```
Pruned Weight = Weight × Sigmoid(Gate)
```

The model is trained with:

```
Total Loss = Classification Loss + λ × Sparsity Loss
```

This forces the network to:

* Keep important weights
* Remove unnecessary weights

---

# 🏃 Training

Run training:

```bash
python experiments/run_experiments.py
```

Training runs for multiple sparsity strengths:

```python
lambdas = [1e-5, 1e-4, 1e-3]
```

---

# 📈 Evaluation



# 📊 Output Example

```
Lambda | Accuracy | Sparsity
1e-5   | 78.32    | 12.45%
1e-4   | 76.81    | 34.21%
1e-3   | 72.15    | 58.93%
```

---

# 📉 Gate Distribution

The project also plots **gate distribution** to visualize pruning behavior.

```
Gate Value Distribution Histogram
```

---

# 🎯 Use Cases

* Model Compression
* Efficient AI
* Edge Deployment
* Research Experiments
* Neural Architecture Optimization

---

# 🛠️ Tech Stack

* Python
* PyTorch
* NumPy
* Matplotlib
* CIFAR-10

---

# 🔬 Future Improvements

* CNN Version
* ResNet Pruning
* Structured Pruning
* Knowledge Distillation
* Quantization

---


AI Engineer | Machine Learning | Deep Learning

---


