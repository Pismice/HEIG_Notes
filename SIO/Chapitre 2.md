# 2.1 Programmation linéaire
## Marche à suivre
Optimisation linéaire = programmation linéaire (problème d'optimisation)
1. Définir les variables de décision
2. Fonction objectif (a maximiser ou minimiser)
3. Modéliser les contraintes (attention à ne pas oublier les quantités non négatives)
4. Final: (s.c. = sous les contraintes)
![](images/Pasted%20image%2020231115132903.png)
## Interprétation géométrique des contraintes
Correspond au *domaine admissble D*
![](images/Pasted%20image%2020231115133255.png)
## Résolution graphique dans le plan
#question pq parallel ?
![](images/Pasted%20image%2020231115133613.png)
## Résultat d'une optimisation linéaire
- **vide**: aucune solution admissible
- **borné**: au moins 1 solution optimale peu importe la fonction objectif
- **non-borné**: #question 
# 2.2 Forme canonique d'une PL et transformation de contraintes
- Problème de *maximisation*
- Toutes les variables sont *non négatives*
- Toutes les autres contraintes sont du type *<=* (on ne compte plus la non-négativité)
![](images/Pasted%20image%2020231115135050.png)
## Règles de transformation
![](images/Pasted%20image%2020231115135234.png)
![](images/Pasted%20image%2020231115135258.png)
## Exemple de mise sous forme canonique
![](images/Pasted%20image%2020231115135348.png)
![](images/Pasted%20image%2020231115135428.png)
# 2.3 Techniques de linéarisation
#todo #question
# 2.4 Résolution de PL avec GLPK et modélisation GMPL
## Format LP
![](images/Pasted%20image%2020231115135945.png)
## Format GMPL
![](images/Pasted%20image%2020231115140048.png)
![](images/Pasted%20image%2020231115140207.png)
![](images/Pasted%20image%2020231115140233.png)
# 2.5 Analyse de sensibilité
#todo  
# 2.6 Programmes linéaires en nombres entiers
# 2.7 Techniques de modélisation à l'aide de variables binaire ou entières
# 2.8 Résolution de PLNE