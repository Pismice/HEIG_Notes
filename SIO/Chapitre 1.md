### 1.1
Types de problèmes difficiles (algo d'approximation~=heuristique) :
- Voyageur de commerce
- Stable cardinal
- Optimisation linéaire
- Bin packing

**Heuristique constructives**: Elaboration pas à pas (pas de solution complète)
**Heuristique d'amélioration (recherche locale)**: Part d'une solution admissible (ex: à l'aide d'une heuristique constructive) et de modifier de solution avec des *échanges* pour trouver une meilleur solution 

### 1.2
Trouver le nb minimum de couleurs pour un graphe: *nombre chromatique*

Méthodes de coloration séquentielle (méthodes gloutonnes): heuristiques constructives qui traitent les sommets les 1 après les autres en essayant d'utiliser les couleurs déjà utilisées sinon -> nouvelle couleur (ex de variantes: choix de l'ordre dans lequel les sommets sont coloriés, choix de la couleur à réutiliser lorsque plusieurs choix sont possibles, ...)

Différents ordres:
- ordre décroissant des degrés
- ordre croissant des degrés
- orde lexicographique/aléatoire des sommets

Choix des couleurs:
- couleur la plus ancienne
- couleur la plus récente
- couleur la plus utilisée, la moins utilisée
- couleur au hasard

#### Algo de colorations
Au +, x+1 couleurs, x étant le degré maximal
TOUJOURS PRRENDRE LA COULEUR LA PLUS JEUNE (1,2,3,...)
**"plus grand degré en premier" (largest-first, Welsh Powell)**
O(n+m)
#question faire comme pour SL ?
1. Plus grand degre initial
2. Alpha
![[Pasted image 20231011135152.png]]

**"plus petit degré en dernier (smallest-last, Matula, Marble, Isaccson)"**
O(n+m) n: sommets et m: arêtes
(On fait notre tab normal de gauche à droite)
1. Plus petit degré (dynamique)
2. Plus petit degre initial
3. Ordre alpha NORMAL
	1. On applique l algo de droite à gauche (toujours couleur la plus jeune donc plus à droite dans ce cas)
![[Pasted image 20231011135826.png]]

**DSATUR**
L'ordre de coloration n'est pas défini à l'avance mais construit *dynamiquement*
O(n²)
degré de *SATURATION* = nb de COULEURS différentes voisines (et non purement de voisins)
Perso je fais tableau initial et un tableau des degré de saturation
1. Degre saturation
2. Degre initial
3. Alpha
![[Pasted image 20231011140745.png]]
![[Pasted image 20231011140758.png]]

**RLF (Recursive Largest First, Leighton)**
ATTENTION A L ORDRE
0. Le + de voisins communs avec le dernier enlevé (les hachurés)
1. Degre actuel avec les sommets en moins (nouvaeau graph) (QUE POUR LA 1ERE ITERATION)
2. Degre initial (celui du graphe de base)
3. Alpha
![[Pasted image 20231011141018.png]]
![[Pasted image 20231011141030.png]]

### 1.3
#### Voyageur de commerce (TSP)
NE PAS OUBLIER D'ADDITIONER LES LONGUEURS À LA FIN
*Trouver la tournée (cycle hamiltonien) la plus courte en ne visitant que 1 et 1 seule fois chaque sommet*
Différentes variantes:
- symétrique ou asymétrique, d(i,j) ?= d(j,i)
- inégalité traingulaire, d(i,j) + d(j,k) >= d(i,k)
- euclidiens, Manhattan, ...
Dans le cadre de ce cours: symétrique, inégalite triangulaire et euclidiens (géométriques)
#### **Plus proche voisin**
1. Choisir une ville au hasard (ou la dernière ville ajoutée)
2. Choisir la ville non visitée la plus proche 
3. Répéter tant qu'il y a des villes non visitées
![[Pasted image 20231011143403.png]]
#### **Plus proche voisin par les 2 bouts**
1. Sur chacun des 2 bouts prendre le voisin le plus proche (PAS chacun son tour)
#### **Heuristique gloutonne**
Prendre a chaque fois l'arrete la plus courte (kourskal avec contraintes)
![[Pasted image 20231011143654.png]]
#### **Insertion la moins chère**
1. Partir de 2 villes
2. Inserer les villes les 1 après les autres en provoquant la plus petite augmentation de la longueur totale de la tournée
#### **Insertion la plus éloignée**
1. Partir de 2 villes
2. #question pas compris mais en gros inserer la ville la plus eloignee
#### **Méthode de Christofides**
1. Kurskal: plus petite arrete a chaque fois (pas de contrainte, il faut juste toucher tous les sommets)
2. Marque tous les sommets de degre impair
3. Relier avec les arretes totales les moins longues possibles chaque sommet marqué (couplage  parfait de poids min)
4. Chemin final: partir de la ville demandée (toujours aller vers la plus petit sommet) avec les raccourcis si reviens en arriere
![[Pasted image 20231011145214.png]]
![[Pasted image 20231011145225.png]]

#### **Meilleure fusion (Clarke et Wright)**
1. Faire la matrice des epargnes (pour tout sauf le depot central): Sij = S1i + S1j - Sij 
2. Prendre les plus grandes valeur de la matrice d'épargne (pas faire de dégre 3 et MARQUE L INDEX SUR LE GRAPHE)
3. Quand il reste 2 sommets (hors dépot central), relier les 2 sommets au déppot central
!!! pas oublier la longueur totale
![[Pasted image 20231011145411.png]]

### 1.4 Heuristiques d'amélioration et d'échanges
Principe: Il est facile de trouver une solution admissible (éventuellement de mauvaise qualité, puis de la modifier)

**Algorithme de descente**
Variante 1: premier voisin améliorant
Variante 2: meilleur voisin améliorant

**k-opt**
*2-opt*
![[Pasted image 20231012184054.png]]
*3-opt*
![[Pasted image 20231012184105.png]]

### 1.5 Brève introduction aux métaheuristiques
#questin recuit simulé algo ? voir exos
# Conclusion
![[Pasted image 20231012184148.png]]