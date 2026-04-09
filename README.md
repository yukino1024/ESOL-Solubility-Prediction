这里是为你准备的 README.md 的完整 Markdown 源码。你可以直接复制并粘贴到你 GitHub 仓库的 README.md 文件中。

Markdown
# ESOL-Solubility-Prediction: A Comparative Study of ML & GNN
# ESOL溶解度预测：机器学习与图神经网络的对比研究

## 🔬 Project Overview | 项目概览
This project is an **AI4Science** exploration focused on predicting aqueous solubility ($\log$ mol/L) using the **ESOL (Delaney)** dataset. The core objective is to evaluate the synergy between traditional chemical domain knowledge and modern representation learning.

本项目是一个 **AI4Science** 探索项目，旨在利用 **ESOL (Delaney)** 数据集预测分子的水溶性（$\log$ mol/L）。核心目标是评估传统化学领域知识与现代表征学习之间的协同作用。

---

## 📂 Modules | 模块说明

### 1. Feature Engineering | 特征工程 (`feature_get.ipynb`)
Extracts multi-scale chemical information using **RDKit**:

利用 **RDKit** 提取多尺度化学信息：
* **Atomic Features**: Atomic number, degree, aromaticity, and hybridization.

  **原子级特征**：原子序数、度数、芳香性、杂化轨道等。
* **Expert Descriptors**: MolLogP (hydrophobicity), TPSA, Molecular Weight, and Valence Electrons.
  
  **专家描述符**：MolLogP（脂水分配系数）、TPSA、分子量、价电子数等。
* **Data Packaging**: Converting SMILES into PyTorch Geometric `Data` objects for GNN training.
  
  **数据封装**：将 SMILES 转化为 PyTorch Geometric 的 `Data` 对象，以便 GNN 训练。

### 2. Machine Learning Baselines | 机器学习基准 (`machine_learning.ipynb`)
Establishes performance benchmarks using classical algorithms on 1D expert features:

利用经典算法在 1D 专家特征上建立性能基准：
* **Models**: Random Forest (RF) and XGBoost.
  
  **模型**：随机森林 (RF) 与 XGBoost。
* **Insight**: Assessing the predictive power of standardized physicochemical descriptors.
  
  **洞察**：评估经过标准化的物理化学描述符的预测能力。

### 3. Neural Architecture Exploration | 神经架构探索 (`MLP.ipynb` & `GNN.ipynb`)
Investigates different deep learning approaches for molecular regression:
研究用于分子回归的不同深度学习方法：
* **MLP**: Analyzing convergence with global molecular descriptors.
  
  **MLP**：基于全局分子描述符分析模型的收敛性。
* **Hybrid GNN**: Implementing a **GCN** (Graph Convolutional Network) architecture that fuses learned graph embeddings with expert $u$ features.
  
  **混合 GNN**：实现基于 **GCN**（图卷积网络）的架构，将学习到的图嵌入与专家特征 $u$ 进行融合。



---

## 🛠️ Tech Stack | 技术栈
* **Cheminformatics (化学信息学)**: RDKit
* **Deep Learning (深度学习)**: PyTorch, PyTorch Geometric (PyG)
* **Machine Learning (机器学习)**: Scikit-learn, XGBoost
* **Data Science (数据科学)**: Pandas, NumPy, Matplotlib
