---
tags: [EE] 
---
Created: 2022-12-03

Assessing the use of Tree Search algorithms in solving Connect-4

Which search algorithm out of Monte-Carlo Tree Search and Optimized Minimax Search is the best in playing Connect-4 in terms of performance and time complexity for increasing grid sizes ?

Évaluation de l'Utilisation de la Recherche Arborescente de Monte-Carlo et de la Recherche Minimax dans Puissance 4

Quel algorithme de recherche, parmi la recherche arborescente de Monte-Carlo et la recherche Minimax optimisée, est le meilleur pour jouer au jeu Puissance 4 en termes de performance et de complexité temporelle pour des tailles de grille croissantes ?

1. Introduction
2. Contexte Théorique
	1. Jeu de Puissance 4
	2. Recherche Minimax
		- Élagage alpha-bêta
		- Fonction d'évaluation
	3. Recherche Arborescente de Monte-Carlo (MCTS)
		- Sélection
		- Expansion
		- Simulation (ou Déploiement)
		- Rétropropagation
3. Hypothèses et Théorie Appliquée
4. Méthodologie Expérimentale
	1. Variables Indépendantes
	2. Variables Dépendantes
	3. Variables Contrôlées
	4. Procédure Expérimentale
4. Résultats Expérimentaux
	1. Aperçu des Résultats
	2. Graphique de l'algorithme MCTS contre Minimax
5. Analyse et Discussion des Résultats
6. Conclusion


---
In general, Monte-Carlo Tree Search (MCTS) and Minimax search are two different algorithms that are commonly used for playing games like Connect-4. MCTS is a probabilistic search algorithm that uses random sampling to explore potential moves and select the best move, whereas Minimax is a deterministic search algorithm that considers all possible moves and selects the move that will result in the best outcome for the player.

In terms of performance and time complexity, MCTS typically outperforms Minimax on larger grid sizes because it is able to explore a larger portion of the game tree in a shorter amount of time. This is because MCTS uses random sampling to explore potential moves, which allows it to quickly discard suboptimal moves and focus on the most promising ones. In contrast, Minimax must explore the entire game tree in order to make a decision, which can be very time-consuming on large grid sizes.

Additionally, MCTS can be easily parallelized, which means that it can take advantage of multiple processors or computers to speed up the search process. This can further improve its performance on large grid sizes.

Overall, MCTS is typically the better choice for playing Connect-4 on larger grid sizes due to its superior performance and time complexity. However, it is worth noting that both algorithms have their own strengths and weaknesses, and the best choice may depend on the specific requirements of the problem at hand.


Sure, here is an introduction to Monte-Carlo Tree Search (MCTS) and Minimax search, two algorithms commonly used for playing games like Connect-4:

Monte-Carlo Tree Search (MCTS) is a probabilistic search algorithm that uses random sampling to explore potential moves and select the best one. It is a popular choice for playing games because it is able to quickly find high-quality moves without having to explore the entire game tree.

Minimax search, on the other hand, is a deterministic search algorithm that considers all possible moves and selects the one that will result in the best outcome for the player. It is a classic algorithm for playing games, but it can be very time-consuming on large grid sizes.

Both algorithms have their own strengths and weaknesses, and the best choice may depend on the specific requirements of the problem at hand. In general, however, MCTS is typically the better choice for playing Connect-4 on larger grid sizes due to its superior performance and time complexity.