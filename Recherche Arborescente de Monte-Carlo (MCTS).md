---
tags: [EE] 
---
Created: 2022-12-20

Monte-Carlo tree search or MCTS is a tree-based algorithm that identifies possible game combinations \cite{mf}. Similarly to the Minimax search it has different branches and sub-branches that indicates possible game configurations. 




In Monte-Carlo tree search, the nodes will not be assigned a value based on an board evaluation but on two values, the number of times the node has been visited and also the number of times this node has led to a victory \cite{mf}. Essentially Monte-Carlo tree search 