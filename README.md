# 🚀 GridlessGo - AI-Powered Wireless EV Charging System

## 🌟 Overview

GridlessGo revolutionizes electric vehicle charging through dynamic wireless charging roads powered by intelligent routing algorithms. Our system eliminates charging downtime by enabling EVs to charge while in motion using embedded road coils and AI-optimized routing.

## 📂 Repository Contents

### 1. [AI Route Optimization & Queue Management](route_optimization.ipynb)
**Core Features:**
- 🗺️ **5x5 Campus Road Network** modeling with NetworkX
- ⚡ **Charging Road Integration** (vertical road at x=2)
- 🚗 **E-Rickshaw Simulation**:
  - Multiple vehicles with varying battery levels (15-60%)
  - Different speeds (60-90 m/min)
  - Real-time location tracking
- 🛣️ **Smart Routing**:
  - Dijkstra's algorithm with traffic-weighted edges
  - Dynamic ETA calculation considering:
    ```python
    travel_time = (path_length * 5) / speed
    ```
  - Priority-based queue sorting (low battery first)
- 📊 **Visualization**:
  - Charging road highlighted in red
  - Vehicle paths color-coded by ID
  - Start locations marked distinctly

**Sample Output:**

<img width="658" alt="Screenshot 2025-05-01 at 12 49 42 PM" src="https://github.com/user-attachments/assets/74b15ba1-0dc9-4ec9-9ede-174d2e382f7f" />
<img width="492" alt="Screenshot 2025-05-01 at 12 49 30 PM" src="https://github.com/user-attachments/assets/0e2f029e-0e48-4e13-a6ed-ce8a1a12d44d" />


### 2. [Enhanced Routing with User Feedback](Improved_path_routing_using_user_feedback.ipynb)
**Advanced Features:**
- 🌉 **10x10 City Grid** 
- ⚖️ **Dual-Algorithm Comparison**:
  - Traditional Dijkstra (blue path)
  - Q-Learning with feedback (red path)
- 🧠 **Reinforcement Learning**:
  ```python
  # Q-table update rule
  Q[state,action] += α*(reward + γ*max(Q[next_state]) - Q[state,action])
  ```
- Action space: 4-direction movement
- Reward function penalizes bad zones
- User Feedback Integration
- 📊 **Visualization**:
  - Side-by-side path plotting
  - Edge weights displayed

**Sample Output:**

<img width="962" alt="Screenshot 2025-05-01 at 12 57 04 PM" src="https://github.com/user-attachments/assets/b95387aa-2194-456a-9e95-38dff1c4ff19" />

