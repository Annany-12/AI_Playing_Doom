# Teaching AI to Play Doom: Reinforcement Learning from Scratch

This project demonstrates training reinforcement learning (RL) agents to play **three ViZDoom scenarios** using Stable-Baselines3's PPO algorithm:

1. **Basic** – Move and shoot a stationary enemy.
2. **Defend the Center** – Survive and shoot enemies coming from multiple directions.
3. **Deadly Corridor** – Traverse a narrow corridor while eliminating enemies.

## 🔧 Installation Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/RL_ViZDoom_PPO.git
cd RL_ViZDoom_PPO
```

### 2. Set Up the Python Environment

Use `pip` to install the required dependencies. Run this in the terminal or uncomment the lines in the notebooks:

```bash
pip install gym
pip install vizdoom
pip install stable-baselines3[extra]
pip install opencv-python
pip install imageio
pip install matplotlib
pip install numpy
```

You may also need:

```bash
pip install moviepy
```

---

## 🗂 Folder Structure

```
RL_ViZDoom_PPO/
│
├── RL_Doom_Python.ipynb             # Scenario 1: Basic
├── RL_Doom_Defend_Center.ipynb      # Scenario 2: Defend the Center
├── RL_Doom_Deadly_Corridor.ipynb    # Scenario 3: Deadly Corridor
├── deadly_corridor_cfgs/            # Custom configs for scenario 3
├── README.md
└── videos/
    ├── basic.mp4
    ├── defend_center.mp4
    └── deadly_corridor.mp4
```

---

## ⚙️ Setup Notes

### 🔁 Config Path Fix

You **must update** all `.cfg` paths in the notebooks depending on where you've saved your `ViZDoom` and `scenarios` folder. For example:

```python
game.load_config("path/to/VizDoom/scenarios/deadly_corridor_cfgs/deadly_corridor_custom_1.cfg")
```

### 📁 Custom Scenario Setup (Deadly Corridor)

For `RL_Doom_Deadly_Corridor.ipynb`, you need to:

1. Locate the `scenarios` folder in your ViZDoom environment.
2. Copy the provided `deadly_corridor_cfgs/` folder into `scenarios/`.

So the final structure becomes:

```
vizdoom/scenarios/deadly_corridor_cfgs/deadly_corridor_custom_1.cfg
```

---

## 🚀 Running the Project

You can run each notebook independently:

### 🟢 1. `RL_Doom_Python.ipynb`

* Basic RL model.
* No extra setup needed.
* Uncomment and run the pip install commands at the top.

### 🟡 2. `RL_Doom_Defend_Center.ipynb`

* Intermediate level with more enemies.
* Update config paths if necessary.
* Also requires basic pip installs.

### 🔴 3. `RL_Doom_Deadly_Corridor.ipynb`

* Custom environment with progressive difficulty.
* Requires `deadly_corridor_cfgs/` folder to be placed correctly.
* Update config paths accordingly.

---

## 📽️ Demo Videos

You can download or watch the trained agent in action for each scenario below:

- [Basic Scenario](videos/basic.mp4)
- [Defend the Center](videos/center.mp4)
- [Deadly Corridor](videos/corridor.mp4)

---

## 💡 Tips

* Train with progressively harder config files for Deadly Corridor.
* Save and reload models using `.zip` files.
* Visualize reward graphs to monitor model performance.
* Use rendering (`render=True`) occasionally to inspect what your agent is doing.

---

## 📌 Final Thoughts

This project is a result of continuous debugging, tuning, and experimentation with RL in FPS-style environments. If you're passionate about AI in games, definitely explore extending this with:

* Custom reward functions.
* DQN or A2C algorithms.
* More complex ViZDoom scenarios.

---

## 📫 Contact / Feedback

Feel free to fork the repo, raise issues, or drop a PR! 💻
