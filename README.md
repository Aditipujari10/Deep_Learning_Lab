# Deep Learning Experiments Collection

Welcome to the Deep Learning Experiments repository! This collection contains 8 distinct experiments demonstrating fundamental and advanced concepts in Deep Learning. 

The experiments cover a wide range of topics, from basic Multi-Layer Perceptrons (MLPs) to advanced concepts like Transfer Learning, Retrieval-Augmented Generation (RAG) with Large Language Models, and Explainable AI (XAI). They are implemented using popular frameworks like **TensorFlow/Keras**, **PyTorch**, and **LangChain**.

---

## 📂 Project Structure & Details

### 1. Neural Network Foundations (Dataset: MNIST)
*   **`dl_exp_01.py`** — **Initialization & Optimization**
    *   **Goal:** Understand how different starting weights and learning algorithms affect model training.
    *   **Details:** Compares weight initialization techniques (`RandomNormal`, `Xavier/GlorotUniform`, `HeNormal`) and optimizers (`SGD` vs `Adam`) on a standard MLP.
*   **`dl_exp_02.py`** — **Regularization Techniques**
    *   **Goal:** Learn how to prevent neural networks from "memorizing" training data (overfitting).
    *   **Details:** Compares models using no regularization against models using Dropout, L2 Regularization (Weight Decay), and Batch Normalization.
*   **`dl_exp_03.py`** — **Learning Rate Strategies & Early Stopping**
    *   **Goal:** Optimize the training loop for better convergence and automatic stopping when the model stops improving.
    *   **Details:** Implements a Fixed Learning Rate, Learning Rate Scheduling (Step Decay), and an Early Stopping callback.

### 2. Convolutional Neural Networks (Dataset: CIFAR-10)
*   **`dl_exp_04.py`** — **Simple CNN from Scratch**
    *   **Goal:** Build an image classifier using raw convolutions.
    *   **Details:** Implemented in **PyTorch**, this experiment constructs a basic Convolutional Neural Network with Conv2D, MaxPool, and Linear layers.
*   **`dl_exp_05.py`** — **Transfer Learning with ResNet50**
    *   **Goal:** Use a massive, pre-trained model on a new task to save time and compute.
    *   **Details:** Loads a pre-trained `ResNet50` model. It demonstrates feature extraction (frozen base) followed by fine-tuning (unfreezing top layers).

### 3. Recurrent Neural Networks (Dataset: IMDB Reviews)
*   **`dl_exp_06.py`** — **Sequence Models for Text Classification**
    *   **Goal:** Process sequential data like text to perform sentiment analysis.
    *   **Details:** Compares three fundamental recurrent architectures: `SimpleRNN`, `LSTM` (Long Short-Term Memory), and `GRU` (Gated Recurrent Unit).

### 4. Advanced Applications
*   **`dl_langchain_exp07.py`** — **RAG System with LangChain**
    *   **Goal:** Create an AI bot that answers questions based on a specific website.
    *   **Details:** Implements Retrieval-Augmented Generation (RAG) using `WebBaseLoader`, `FAISS` vector embeddings (`all-MiniLM-L6-v2`), and the Groq API (`llama-3.1-8b-instant`).
*   **`dl_exp8.py`** — **Explainable AI with LIME**
    *   **Goal:** Look inside the "black box" to see *why* a model made a specific prediction.
    *   **Details:** Applies LIME (Local Interpretable Model-agnostic Explanations) to highlight which pixels of an MNIST digit most influenced the MLP's prediction.

---

## 🛠️ Requirements & Installation

Ensure you have the required libraries installed before running the scripts. You can install all dependencies via pip:

```bash
pip install tensorflow torch torchvision numpy matplotlib pandas scikit-image lime langchain langchain-community langchain-core langchain-groq faiss-cpu sentence-transformers beautifulsoup4
```

> **Note:** To run `dl_langchain_exp07.py`, you need a free [Groq API Key](https://console.groq.com/keys). Set it as an environment variable or replace `"YOUR_GROQ_API_KEY"` directly in the script.

## 🚀 How to Run

To execute an experiment, simply run the Python script from your terminal:

```bash
python dl_exp_01.py
```

---

## 📊 Quick Summary Table

Here is a quick overview of what each experiment does:

| Experiment # | Filename | Primary Topic | Key Technologies / Concepts |
| :--- | :--- | :--- | :--- |
| **Exp 01** | `dl_exp_01.py` | Weight Initialization & Optimizers | MLP, MNIST, Adam, SGD, Xavier, HeNormal |
| **Exp 02** | `dl_exp_02.py` | Regularization | Dropout, L2 Regularization, Batch Normalization |
| **Exp 03** | `dl_exp_03.py` | Learning Rate Control | LR Scheduling, Early Stopping, Keras Callbacks |
| **Exp 04** | `dl_exp_04.py` | CNN Basics | **PyTorch**, Convolutional Neural Network, CIFAR-10 |
| **Exp 05** | `dl_exp_05.py` | Transfer Learning | ResNet50, Fine-Tuning, Feature Extraction |
| **Exp 06** | `dl_exp_06.py` | Sequence Modeling (NLP) | RNN, LSTM, GRU, IMDB Sentiment Analysis |
| **Exp 07** | `dl_langchain_exp07.py`| Generative AI & RAG | **LangChain**, Groq LLM, FAISS Vector DB, Web Scraping |
| **Exp 08** | `dl_exp8.py` | Explainable AI (XAI) | LIME, Model Interpretability, Image Segmentation |
