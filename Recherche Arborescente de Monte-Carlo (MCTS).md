---
tags: [EE] 
---
Created: 2022-12-20

Monte-Carlo tree search or MCTS is a tree-based algorithm that identifies possible game combinations \cite{mf}. Similarly to the Minimax search it has different branches and sub-branches. MCTS enables us to navigate enormous state spaces with significantly less constraints than brute-forcing by allowing us to seek for the best movements to play depending on statistics rather than on comprehensive exploration \cite{mcts2} like the Minimax search . Essentially MCTS explores nodes that are promising and the more statistics are collected the better the results will be.

In Monte-Carlo tree search, the nodes will not be assigned a value based on a board evaluation like the Minimax search but on two values, the number of times the node has been visited and also the number of times this node has led to a victory \cite{mf} and we will see why these informations are important to find the best moves later. To explore and choose these promising nodes, MCTS has four steps that we will see in the next subsections: selection, expansion, simulation and backpropagation.

