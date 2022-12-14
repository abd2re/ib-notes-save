---
tags: [physics] 
---
Created: 2022-12-20

# Piles électriques
?
Une pile convertit l'énergie chimique en énergie électrique avec dissipation/perte d'énergie sous forme de chaleur.
<!--SR:!2023-01-25,18,190-->

- Une pile est caractérisée par:: sa fem $e$ et sa résistance interne $r$. $e$ en volt et $r$ en ohm.
<!--SR:!2023-01-21,15,190-->
- $e$ fem =>:: force électromotrice; travail par unité de charge pour faire circular les charges
<!--SR:!2023-01-12,15,246-->

Formule de la tension aux bornes d'une pile est:
?
$$U=e-rI$$- $U$ = tension dans la puissance électrique
- $e$ = fem de la puissance chimique
- $r$ = résistance interne 
- $I$ = intensité
- ![[Piles électriques-6.png]]
<!--SR:!2023-01-21,16,226-->

Caractéristique intensité-tension d'une pile (graphe)::![[Piles électriques.png]]
<!--SR:!2023-02-14,34,246-->

On peut retrouver la formule $U=e-rI$ en effectuant le montage suivant::![[circuit caractéristique d'une pile]]
<!--SR:!2023-02-11,34,246-->

- $U=e$ si:: $I=0$
<!--SR:!2023-02-08,32,246-->
- $e$ c'est la tension aux bornes de la pile quand:: elle ne fournit pas de courant
<!--SR:!2023-01-13,16,246-->
- Un pile idéale est une pile qui:: n'a pas de résistance interne $r=0$ (le graphe intensité-tension est constante en $e$)
<!--SR:!2023-02-12,33,246-->

circuit équivalent d'une pile réel::![[equivalent e;r]]
<!--SR:!2023-01-30,25,246-->

## Circuits avec des piles
formule emf::$$e=(r+R)I$$
<!--SR:!2023-01-31,22,226-->


## Circuits simples comportant des piles, récepteurs et resistors

**Tension aux bornes d'un récepteur**:
?
Un récepteur (ex un moteur, un électrolyseur) est un appareil qui consomme plus d'énergie que n'a besoin l'effet joule.
Le récepteur est caractérisé oar 1 fcem $e'$ (force contre électromotrice) et par sa résistance interne. 
<!--SR:!2023-01-16,5,240-->

Formule de la tension  d'un récepteur::$$U_{recept}=e'+rI$$
<!--SR:!2023-01-17,6,240-->
- Une pile branchée en opposition se comporte comme:: un récepteur
<!--SR:!2023-01-16,5,240-->


Formule des fem et fcem dans un circuit avec piles et récepteurs (+branchement):
?
![[image-20230109163848957.png]]
$$\Sigma{e} - \Sigma{e'}=\Sigma{R}\times I$$
<!--SR:!2023-01-15,4,240-->

## Circuit avec des nœuds comportant des générateurs

Schema du sens de parcours (rouge) et sens du courant (bleu) pour les piles et les résistances:
?
![[image-20230109170117486.png]]
<!--SR:!2023-01-17,6,240-->

## Association de piles
**En série** (Avantage, branchement et formule)
?
Pour avoir plus de tension.
![[image-20230110091918045.png]]$$V_{PN}=V_{PA}+V_{AB}+V_{BN}$$
$$V_{PN}=e_{1}-r_{1}I+e_{2}-r_{2}I+e_{3}-r_{3}I$$
$$V_{PN}=e_{1}+e_{2}+e_{3}-(r_{1}+r_{2}+r_{3})I$$
$$e_s=\sum{e}$$$$r_s=\sum\limits{r}$$
<!--SR:!2023-01-12,2,240-->

**En parallèle** (Avantage, branchement et formule)
?
Pour avoir plus d'intensité
![[image-20230110093433182.png]]
$$U_{PN}=e-r\frac{I}{n}=e-r\frac{I}{n}=e-r\frac{I}{n}$$
$$e_{//}=e,\;r_{//}=\frac{r}{n}$$
<!--SR:!2023-01-12,2,240-->









