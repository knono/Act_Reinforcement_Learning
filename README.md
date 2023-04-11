## Summary
Frozen lake involves crossing a frozen lake from Start(S) to Goal(G) without falling into any Holes(H) by walking over the Frozen(F) lake.
The agent may not always move in the intended direction due to the slippery nature of the frozen lake.

![grid_FrozenLake.png](attachment:10bbfc95-6918-4b07-a8cf-aa2fda74b92e.png)
      
**Action Space**
The agent takes a 1-element vector for actions. The action space is `(dir)`, where `dir` decides direction to move in which can be:
* 0: LEFT
* 1: DOWN
* 2: RIGHT
* 3: UP

The symbols when you show the render mean the following:
* S, Starting point, safe
* F, Frozen surface, safe
* H, Hole, fall to your doom
* G, Goal, where the frisbee is located


**Observation Space** The observation is a value representing the agent's current position as current_row * nrows + current_col (where both the row and col start at 0). For example, the goal position in the 4x4 map can be calculated as follows: 3 * 4 + 3 = 15. The number of possible observations is dependent on the size of the map. For example, the 4x4 map has 16 possible observations.

**Rewards** Reward schedule:
* Reach goal(G): +1
* Reach hole(H): 0
* Reach frozen(F): 0
