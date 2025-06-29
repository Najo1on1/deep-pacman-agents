# Deep Pac-Man Agents with DQN, Double DQN & Dueling Architectures

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yourusername/deep-pacman-agents/blob/main/notebooks/Intro_to_DQN.ipynb)  
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 🕹️ Quick Demo

**Vanilla DQN (ε-greedy)**  
![Vanilla DQN](https://i.imgur.com/9ru85kU.gif)

**Double DQN + UCB**  
![DDQN + UCB](https://i.imgur.com/bBWylLN.gif)

**Dueling Double DQN + UCB**  
![Dueling DDQN + UCB](https://i.imgur.com/cCDxclc.gif)

---

## 📥 How to Reproduce

1. **Clone the repo**  
   ```bash
   git clone https://github.com/yourusername/deep-pacman-agents.git
   cd deep-pacman-agents
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the notebook**  
   ```bash
   jupyter notebook notebooks/Intro_to_DQN.ipynb
   ```

4. **(Optional) Run from Colab**  
   Click the “Open in Colab” badge above to launch in Google Colab.

---

## 🛠️ Highlights of the Approach

- **Why RL for Pac-Man?**  
  - Sequential decision-making under uncertainty  
  - Sparse, delayed rewards map naturally to Q-learning

- **The Environment**  
  - Arcade Learning Environment via Gym (`ale-py`, `gym[atari]`)  
  - Frame preprocessing: grayscale, resizing, frame-stacking

- **Vanilla DQN**  
  - **Data capture & preprocessing**: state buffer, ε-greedy episodes  
  - **Network architecture**: convolutional encoder + fully connected Q-head  
  - **Training**: 100,000 episodes, Adam optimizer, MSE loss  
  - **Results & evaluation**: reward curves, Wilcoxon tests for performance growth

- **Double DQN + UCB Exploration**  
  - **Motivation**: reduce value overestimation  
  - **Implementation**: target network decoupling + Upper-Confidence-Bound bonus  
  - **Outcome**: smoother learning curve, higher average scores

- **Dueling Double DQN + UCB**  
  - **Architecture**: separate value & advantage streams  
  - **Exploration**: UCB bonus retains optimistic exploration  
  - **Impact**: faster convergence, more strategic gameplay

- **Qualitative Gameplay Comparison**  
  - Side-by-side GIFs demonstrate “smarter” behavior (cornering, ghost avoidance)

---

## 📜 Requirements

<details>
<summary>Click to expand <code>requirements.txt</code></summary>

```text
ale-py>=0.8.1
gym[atari]>=0.25.0
numpy>=1.21
pandas>=1.3
matplotlib>=3.4
scikit-learn>=0.24
scipy>=1.7
torch>=1.10
torchvision>=0.11
opencv-python>=4.5
```
</details>

---

## ⚖️ License & Contact

This project is released under the **MIT License**.  
See [LICENSE](LICENSE) for details.

Questions or feedback?  
– GitHub: [@yourusername](https://github.com/yourusername)  
– Email: your.email@example.com

---

## 📚 References

- Mnih et al., “Human-level control through deep reinforcement learning,” *Nature*, 2015.  
- Wang et al., “Dueling Network Architectures for Deep Reinforcement Learning,” *ICML*, 2016.  
- Double DQN: van Hasselt et al., *AAAI*, 2016.  
