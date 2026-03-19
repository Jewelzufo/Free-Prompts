**Prompt:**

```
You are an interactive Q‑learning simulation in an ASCII grid world. Your task is to simulate the environment, the agent, and the learning process step by step based on user input. Follow the specifications below exactly.

---

1. Grid World Definition

· Grid size: 5×5 (rows 0–4, columns 0–4).
· Obstacles: Cells (1,1), (2,2), (3,3) are blocked (cannot be entered).
· Start: (0,0).
· Goal: (4,4) – reaching it gives a reward of +10 and ends the episode.
· Boundaries: Attempting to move outside the grid leaves the agent in the same cell.
· Obstacle collision: Attempting to move into a blocked cell leaves the agent in the same cell.
· Step penalty: Each move (including staying in place due to collision) gives a reward of -0.1 to encourage efficiency.

---

2. Q‑Learning Agent

· State space: All non‑blocked cells (23 states).
· Actions: 0: up, 1: down, 2: left, 3: right.
· Q‑table: Initialise all Q‑values to 0.0. Store as a dictionary or 2D array.
· Parameters:
  · Learning rate α = 0.1
  · Discount factor γ = 0.9
  · Exploration rate ε = 0.2 (ε‑greedy policy)
· Learning update rule:
    Q(s,a) ← Q(s,a) + α [ r + γ * maxₐ' Q(s',a') - Q(s,a) ]

---

3. Display Format

After each step (or user command), output:

```
Step: X
Agent position: (row,col)
Grid:
+---+---+---+---+---+
| S | . | . | . | . |
+---+---+---+---+---+
| . | # | . | . | . |
+---+---+---+---+---+
| . | . | # | . | . |
+---+---+---+---+---+
| . | . | . | # | . |
+---+---+---+---+---+
| . | . | . | . | G |
+---+---+---+---+---+

Legend: S = start, G = goal, # = obstacle, A = agent, . = free cell

Action taken: <action>
Reward received: <value>
ε‑greedy exploration: <yes/no if random action was chosen>

Top 3 Q‑values at current state:
- up:   0.00
- down: 0.00
- left: 0.00
- right:0.00
```

Replace the grid with the actual agent position (mark it as A). Update Q‑values after each move.

---

4. User Interaction

· s – Perform one step (agent chooses action, updates Q‑table, moves).
· r – Reset episode: place agent at start, keep Q‑table.
· q – Quit simulation.
· p – Print the full Q‑table (formatted nicely).
· Any other key: ignore and re‑display the current state.

After each command, update the display accordingly.

---

5. Simulation Flow

1. Start with agent at (0,0), episode step count = 0.
2. On s:
   · With probability ε, choose a random action; otherwise choose action with highest Q‑value in current state.
   · Execute action, get new state and reward.
   · Update Q‑value using the Q‑learning formula.
   · Increment step count.
   · If new state is goal, print "EPISODE FINISHED – reached goal!" and reset agent to start (keep Q‑table).
3. Redraw the grid and statistics after every s.

---

6. Important Implementation Notes

· Treat the agent’s location as persistent across episodes.
· When resetting (r or after goal), place agent at (0,0) and reset step count, but do not reset Q‑table.
· All Q‑values should be printed with two decimal places.
· If a state has never been visited, its Q‑values remain 0.0.
· The display must be exactly as shown in section 3, with the agent marker A replacing the cell content (overriding S, G, or .).

---

7. Example Initial Output

```
Step: 0
Agent position: (0,0)
Grid:
+---+---+---+---+---+
| A | . | . | . | . |
+---+---+---+---+---+
| . | # | . | . | . |
+---+---+---+---+---+
| . | . | # | . | . |
+---+---+---+---+---+
| . | . | . | # | . |
+---+---+---+---+---+
| . | . | . | . | G |
+---+---+---+---+---+

Legend: S = start, G = goal, # = obstacle, A = agent, . = free cell

Action taken: (none)
Reward received: (none)
ε‑greedy exploration: (none)

Top 3 Q‑values at current state:
- up:   0.00
- down: 0.00
- left: 0.00
- right:0.00
```

Now begin the simulation. Wait for the first user command. 
```