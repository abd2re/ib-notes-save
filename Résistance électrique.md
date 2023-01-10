---
tags: [physics] 
---
Created: 2022-12-12

# Résistance électrique
?
Tout les matériaux ne conduisent pas le courant électrique de la meme manière, on définit la résistance électrique comme étant la formule::$$R=\frac{\Delta V}{I}$$
<!--SR:!2023-02-01,31,230-->

La résistance d'un fil conducteur a comme formule:
?
$$R=\frac{\rho l}{A}$$
- $R$ est la résistance en Ohm ($\Omega$)
- $\rho$ est la résistivité du matériau en ohm-metre
- $l$ est la longueur du fil
- $A$ est la surface du fil
<!--SR:!2023-01-27,28,230-->

## Loi d'Ohm et conducteur ohmique

Caractéristique intensité-tension du resistor a comme graphe::![[Résistance électrique.png]]
<!--SR:!2023-01-28,28,230-->
- Formule de la loi d'Ohm::$$U=RI$$ car $U$ et $I$ sont proportionnelles.
<!--SR:!2023-02-07,34,230-->

- Loi d'Ohm:: A température constante la tension et l'intensité aux bornes d'un conducteurs sont proportionnelles
<!--SR:!2023-01-14,7,170-->
- Un conducteur ohmique:: est un conducteur qui obéit a la loi d'Ohm ($R$ est constant)![[Résistance électrique-1.png]]
<!--SR:!2023-01-12,20,250-->

## Association de résistors
- Association en série formule::$$R_{eqs}=R_1+R_2+\text{...}$$ l'association en série de plusieurs résistors est équivalent a un résistor $R_{eqs}$ dont la résistance est égale a la somme des résistances
<!--SR:!2023-02-04,33,242-->
- Association en parallèle formule::$$\frac{1}{R_{eqp}}=\frac{1}{R_{1}}+\frac{1}{R_{2}}+\text{...}$$ $$R_{eqp}=\frac{R_{1}R_{2}}{R_{1}+R_{2}}$$
<!--SR:!2023-01-29,29,241-->

## Dissipation d'énergie électrique dans un resistor (effet joule)
?
Lorsque qu'un conducteur est parcouru par un courant électrique il y a un dégagement de chaleur: c'est l'effet joule. 
Pour lutter contre l'effet joule on prévoit des dispositifs d'aération ou de ventilation. L'effet joule est utilisé avantageusement dans les plaques chauffantes, les fusibles, les chauffe-eau.
<!--SR:!2023-01-14,18,222-->

La puissance dissipé par effet joule est proportionnelle:: au carré de l'intensité.
<!--SR:!2023-01-17,17,222-->

3 formules de puissance dissipé::$$P=UI=RI^2=\frac{U^{2}}{R}$$
<!--SR:!2023-02-06,34,242-->

## Utilisation des appareils de mesure
Un appareil de mesure modifie le circuit et a un effet sur la mesure. 

- Utilisation d'un ampèremètre: un ampèremètre idéal:: a une résistance interne nulle
<!--SR:!2023-01-25,27,242-->
- Utilisation d'un voltmètre: un voltmètre idéal:: a une résistance interne infinie
<!--SR:!2023-02-10,36,242-->

## Diviseur de tension et montage potentiométrique
Formule et circuit
?
![[image-20221220093220947.png]]
$$U=(R_{1}+R_{2})\times I$$
donc
$$I=\frac{U}{R_{1}+R_{2}}$$
On sait que
$$U_{1}=R_{1}\times I$$
donc
$$U_{1}=R_{1}\times \frac{U}{R_{1}+R_{2}}=\boxed{\frac{R_1}{R_{1}+R_{2}}\times U}$$
<!--SR:!2023-02-06,29,240-->




