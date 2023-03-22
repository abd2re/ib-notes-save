---
tags: [physics] 
---
Created: 2022-12-20

# Piles électriques
?
Une pile convertit l'énergie chimique en énergie électrique avec dissipation/perte d'énergie sous forme de [[chaleur]].
<!--SR:!2023-05-16,70,190-->

- Une pile est caractérisée par:: sa fem $e$ et sa résistance interne $r$. $e$ en volt et $r$ en ohm.
<!--SR:!2023-03-23,40,286-->

<!--SR:!2023-02-27,33,190-->
- $e$ fem =>:: force électromotrice; travail par unité de charge pour faire circular les charges
<!--SR:!2023-05-20,91,246-->

Formule de la tension aux bornes d'une pile est:
?
$$U=e-rI$$- $U$ = tension dans la puissance électrique
- $e$ = fem de la puissance chimique
- $r$ = résistance interne 
- $I$ = intensité
- ![[Piles électriques-6.png]]
<!--SR:!2023-06-21,99,226-->

Caractéristique intensité-tension d'une pile (graphe)::![[Piles électriques.png]]
<!--SR:!2023-05-12,86,246-->

On peut retrouver la formule $U=e-rI$ en effectuant le montage suivant::![[circuit caractéristique d'une pile]]
<!--SR:!2023-05-06,84,246-->

- $U=e$ si:: $I=0$
<!--SR:!2023-04-25,76,246-->
- $e$ c'est la tension aux bornes de la pile quand:: elle ne fournit pas de courant
<!--SR:!2023-05-25,94,246-->
- Un pile idéale est une pile qui:: n'a pas de résistance interne $r=0$ (le graphe intensité-tension est constante en $e$)
<!--SR:!2023-05-04,81,246-->

circuit équivalent d'une pile réel::![[equivalent e;r]]
<!--SR:!2023-04-04,63,246-->

## Circuits avec des piles
formule emf::$$e=(r+R)I$$
<!--SR:!2023-07-13,113,226-->


## Circuits simples comportant des piles, récepteurs et resistors

**Tension aux bornes d'un récepteur**:
?
Un récepteur (ex un moteur, un électrolyseur) est un appareil qui consomme plus d'énergie que n'a besoin l'effet joule.
Le récepteur est caractérisé oar 1 fcem $e'$ (force contre électromotrice) et par sa résistance interne. 
<!--SR:!2023-05-14,74,240-->

Formule de la tension  d'un récepteur::$$U_{recept}=e'+rI$$
<!--SR:!2023-06-15,94,240-->
- Une pile branchée en opposition se comporte comme:: un récepteur
<!--SR:!2023-06-15,96,240-->


Formule des fem et fcem dans un circuit avec piles et récepteurs (+branchement):
?
![[image-20230109163848957.png]]
$$\Sigma{e} - \Sigma{e'}=\Sigma{R}\times I$$
<!--SR:!2023-05-13,74,240-->

## Circuit avec des nœuds comportant des générateurs

Schema du sens de parcours (rouge) et sens du courant (bleu) pour les piles et les résistances:
?
![[image-20230109170117486.png]]
<!--SR:!2023-06-25,101,240-->

## Association de piles
**En série** (Avantage, branchement et formule)
?
Pour avoir plus de tension.
![[image-20230110091918045.png]]$$V_{PN}=V_{PA}+V_{AB}+V_{BN}$$
$$V_{PN}=e_{1}-r_{1}I+e_{2}-r_{2}I+e_{3}-r_{3}I$$
$$V_{PN}=e_{1}+e_{2}+e_{3}-(r_{1}+r_{2}+r_{3})I$$
$$e_s=\sum{e}$$$$r_s=\sum\limits{r}$$
<!--SR:!2023-06-01,84,240-->

**En parallèle** (Avantage, branchement et formule)
?
Pour avoir plus d'intensité
![[image-20230110093433182.png]]
$$U_{PN}=e-r\frac{I}{n}=e-r\frac{I}{n}=e-r\frac{I}{n}$$
$$e_{//}=e,\;r_{//}=\frac{r}{n}$$
<!--SR:!2023-05-15,74,240-->








