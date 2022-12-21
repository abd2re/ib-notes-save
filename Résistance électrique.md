---
tags: [physics] 
---
Created: 2022-12-12

# Résistance électrique
?
Tout les matériaux ne conduisent pas le courant électrique de la meme manière, on définit la résistance électrique comme étant la formule::$$R=\frac{\Delta V}{I}$$
<!--SR:!2023-01-01,12,230-->

La résistance d'un fil conducteur a comme formule:
?
$$R=\frac{\rho l}{A}$$
- $R$ est la résistance en Ohm ($\Omega$)
- $\rho$ est la résistivité du matériau en ohm-metre
- $l$ est la longueur du fil
- $A$ est la surface du fil
<!--SR:!2022-12-30,11,230-->

## Loi d'Ohm et conducteur ohmique

Caractéristique intensité-tension du resistor a comme graphe::![[Résistance électrique.png]]
<!--SR:!2022-12-31,11,230-->
- Formule de la loi d'Ohm::$$U=RI$$ car $U$ et $I$ sont proportionnelles.
<!--SR:!2022-12-21,6,230-->

- Loi d'Ohm:: A température constante la tension et l'intensité aux bornes d'un conducteurs sont proportionnelles
<!--SR:!2022-12-24,4,190-->
- Un conducteur ohmique:: est un conducteur qui obéit a la loi d'Ohm ($R$ est constant)![[Résistance électrique-1.png]]
<!--SR:!2022-12-23,8,250-->

## Association de résistors
- Association en série formule::$$R_{eqs}=R_1+R_2+\text{...}$$ l'association en série de plusieurs résistors est équivalent a un résistor $R_{eqs}$ dont la résistance est égale a la somme des résistances
<!--SR:!2023-01-02,13,242-->
- Association en parallèle formule::$$\frac{1}{R_{eqp}}=\frac{1}{R_{1}}+\frac{1}{R_{2}}+\text{...}$$ $$R_{eqp}=\frac{R_{1}R_{2}}{R_{1}+R_{2}}$$
<!--SR:!2022-12-31,11,241-->

## Dissipation d'énergie électrique dans un resistor (effet joule)
?
Lorsque qu'un conducteur est parcouru par un courant électrique il y a un dégagement de chaleur: c'est l'effet joule. 
Pour lutter contre l'effet joule on prévoit des dispositifs d'aération ou de ventilation. L'effet joule est utilisé avantageusement dans les plaques chauffantes, les fusibles, les chauffe-eau.
<!--SR:!2022-12-27,7,222-->

La puissance dissipé par effet joule est proportionnelle:: au carré de l'intensité.
<!--SR:!2022-12-21,6,242-->

3 formules de puissance dissipé::$$P=UI=RI^2=\frac{U^{2}}{R}$$
<!--SR:!2023-01-03,14,242-->

## Utilisation des appareils de mesure
Un appareil de mesure modifie le circuit et a un effet sur la mesure. 

- Utilisation d'un ampèremètre: un ampèremètre idéal:: a une résistance interne nulle
<!--SR:!2022-12-29,10,242-->
- Utilisation d'un voltmètre: un voltmètre idéal:: a une résistance interne infinie
<!--SR:!2022-12-21,6,242-->

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
<!--SR:!2022-12-22,2,240-->




