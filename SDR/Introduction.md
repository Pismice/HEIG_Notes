## Types de système
*Réparti* : Logique (couplage logiciel fort et couplage matériel faible)
*Distribué* : Architecture infra physique
*Décentralisé* : Absence d'autorité centrale
Distribué/réparti n'implique pas forcément décentralisé mais c'est souvent le cas
## Concurence vs parallélisme
*Concurence* : Les tâches ne s'effectuent pas réellement en même temps mais plutôt un petit moment chacun leur tour
*Parallélisme* : Les tâches s'effectuent en même temps
## Classificatin de Flynn
![[Pasted image 20230925122820.png]]
## Couplage matériel / logiciel
*Couplage fort* = Beaucoup de liens, rapides (Shared memory)
*Couplage faible* = Peu de liens, lents (Distributed memory)
Si le couplage matériel est faible il est préférable de faire pareil pour le couplage logiciel
## Bon système réparti
### 1. Transparence
*Emplacement* : Pas d'adresse phyisque des machines ou données #question
*Migration* : Déplacement des processus/données invisible
*Duplication* : Gestion implicite des copies éventuelles
*Cohérence* : Gestion implicite de la concurrence
### 2. Fiabilité
*Disponibilité* : Résilience aux pannes de machines et de réseau
*Justesse* : Etat toujours correct (recup apres panne, résistance aux attaques)
### 3. Performance
*Parallélisme maximal* : Eviter d'avoir des machines en attente de travail
*Communication minimale* : Diminuer le nb d'échanges de messages
### 4. Dimensionnement
*Extensibilité* : Ajouter une machine doit être possible et peu couteux
*Complexité alogrithmique faible* : Avoir + de machines ne doit pas rendre le service "notablement" plus lent 
=> Eviter les goulots d'étranglement
	- Elément centralisé
	- Nécessité de connaissance d'un état global

### Tradeoff Performance-Fiabilité
Garantir la fiabilité nécessite des procesus limitant les perf
#question Pas compris la phrase

## Synchronisation
![[Pasted image 20230925131619.png]]
## Traitement des erreurs
- Pas de *perte*
- Pas de *duplication*
- Pas de changement d'*ordre*
### Différents protocoles de fiabilité
#### R (aka "peut-être")
![[Pasted image 20230925133511.png]]
#### RR (Request-Reply)
![[Pasted image 20230925133550.png]]
version "Exactment une fois" = avec id 
#### RRA (Request-Reply-Acknowledge)
Une fois acknowledged on supprime l'identificateur
![[Pasted image 20230925141922.png]]

# Exercices
![[Pasted image 20230925142414.png]]

RR "exactement une fois"
![[Pasted image 20230925142509.png]]