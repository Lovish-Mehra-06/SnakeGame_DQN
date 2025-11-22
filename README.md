# SnakeGame_DQN
A Python project that uses Deep Q-Learning (DQN) to train an AI to play Snake. Features include efficient training with experience replay, reward shaping, and optional visualization of training progress.
Here’s a **ready-to-use `README.md`** for your Snake AI project:


---

## Features

- Deep Q-Learning (DQN) based AI for Snake.
- Experience replay and batch training for stable learning.
- Reward shaping for efficient movement and survival.
- Optional Pygame visualization of the snake’s gameplay.
- Automatically saves the best-performing model.

---

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Lovish-Mehra-06/SmartSnakeAI.git
````

2. Navigate to the project directory:

```bash
cd SmartSnakeAI
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Usage

1. Run the training script:

```bash
python agent.py
```

2. To **train faster**, disable rendering in `SnakeGameAI`:

```python
game = SnakeGameAI()
```

3. The **best model** is saved automatically as `model.pth`.

4. To **load a trained model**, the agent will automatically attempt to load `model.pth` if it exists.

---

## How It Works

* The AI observes the game state (danger straight, right, left; direction; food location).
* It chooses moves using an **epsilon-greedy policy**.
* Rewards:

  * Eating food: +10
  * Dying: –10
  * Small movement penalty: –0.01
* Training happens using **short-term memory** (per move) and **long-term memory** (experience replay).

---

## Requirements

* Python 3.7+
* Pygame
* Numpy
* PyTorch
* Matplotlib (optional, for plotting training progress)

---

## Optional Improvements

* Use GPU for faster training.
* Increase network size for higher maximum scores.
* Run multiple snakes in parallel for accelerated experience collection.

---



