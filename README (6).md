# Wids5.0-RL-Stock-Trading
# Reinforcement Learning: From Physics Simulations to Financial Markets

This repository documents the development of reinforcement learning agents across two major academic milestones: a midterm project focused on discrete control and an endterm project centered on complex financial portfolio management.

---

## Midterm Assignment: Lunar Lander v2
**File:** `lunarlanding.ipynb`

The midterm assignment served as a foundation for understanding value-based reinforcement learning. I implemented a **Deep Q-Network (DQN)** to master the Lunar Lander v2 environment provided by Gymnasium.

### Implementation Details:
* **The Goal**: The agent is tasked with landing a spacecraft on a designated pad while managing fuel and orientation.
* **State and Action Space**: The state consists of 8 variables, including coordinates and velocities, while the agent chooses from 4 discrete actions: doing nothing, or firing the left, right, or main engines.
* **Core Mechanics**: I utilized a neural network to approximate the optimal action-value function ($Q^*$). The implementation includes experience replay and a target network to ensure stable training.
* **Outcome**: The agent successfully learned to navigate the physics of the environment, consistently achieving the landing pad and exceeding the 200-point threshold required for success.

---

## Endterm Assignment: NIFTY 50 Trading Agent
**File:** `Untitled11.ipynb`

The final project represents a shift into real-world data application. I developed a custom trading environment based on the "Stock Prediction Ensemble Strategy" paper to manage a portfolio of Indian stocks from the NIFTY 50 index.

### Project Architecture:
* **The Data**: The agent was trained and evaluated on daily historical data (Open, High, Low, Close, and Volume) for major stocks like RELIANCE, HDFCBANK, and TCS between **2010 and 2019**.
* **The Algorithm**: I implemented the **Proximal Policy Optimization (PPO)** algorithm, an actor-critic method, using the Stable-Baselines3 library to handle the continuous decision-making required for market trading.
* **Custom Environment**:
    * **State Space**: The state includes the cash balance, shares currently held, and four technical indicators: **MACD, RSI, CCI, and ADX**.
    * **Action Space**: The agent makes buy, sell, or hold decisions for each stock in the portfolio.
    * **Constraints**: To ensure realism, the environment enforces a **0.1% transaction cost** on every trade and clips actions to ensure the cash balance remains non-negative.

### Performance Summary:
* **Total Cumulative Return**: 44.85%
* **Annualized Sharpe Ratio**: 0.29

---
