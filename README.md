# ♟️ Dynamic Chess AI with Adaptive Evaluation

An intelligent chess engine that combines **Minimax search**, **feature-based evaluation**, and **online learning** using optimization techniques like **Conjugate Gradient** and **Golden Section Search**.

---

## 📌 Overview

This project implements a **self-improving chess AI** that learns from gameplay data and dynamically adapts its evaluation strategy. Unlike traditional engines with static heuristics, this system continuously updates its parameters using replay memory and game outcomes.

It integrates:
- Classical search (Minimax with Alpha-Beta pruning)
- Feature-based evaluation
- Online learning with optimization techniques

📄 Full implementation: see project notebook

---

## ✨ Key Features

- ♟️ Minimax with Alpha-Beta Pruning  
- ⚡ Parallel Move Evaluation using Multiprocessing  
- 🧠 Learnable Evaluation Function (Adaptive Weights)  
- 🔁 Replay Buffer for Experience Storage  
- 📈 Conjugate Gradient Optimization  
- 🔍 Golden Section Search for Parameter Tuning  
- 🎯 Opponent Modeling (Aggression-aware strategy)  
- 📊 Feature Engineering from FEN positions  

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Libraries:**  
  - python-chess  
  - numpy, pandas  
  - tqdm  
  - multiprocessing  
- **Dataset:** Chess.com games dataset (via KaggleHub)

---


---

## 🧠 Methodology

### 1. Feature Engineering

Each chess position is converted into a **5-dimensional feature vector**:
- Material balance  
- Mobility  
- Center control  
- King safety  
- Pawn structure  

---

### 2. Search Algorithm

- Minimax with Alpha-Beta pruning  
- Move ordering based on captures and checks  
- Parallel evaluation for faster decision-making  

---

### 3. Learning Mechanism

#### Conjugate Gradient Optimization

Used to efficiently update evaluation weights by solving:
((2/n) XᵀX + λI)W = (2/n) Xᵀy


---

#### Golden Section Search

Optimizes the **scaling parameter (x)** to improve correlation between predicted and actual outcomes.

---

### 4. Online Learning

- Stores positions in replay buffer  
- Updates weights after each game  
- Performs incremental updates during gameplay  

---

## ▶️ Installation

```bash
git clone https://github.com/your-username/dynamic-chess-ai.git
cd dynamic-chess-ai

pip install -r requirements.txt
