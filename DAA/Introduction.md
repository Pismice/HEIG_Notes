# Outils utlisés
SDK Android : Debugger, build tools, emulateur, bibliotheques logicelles (Java et Kotlin), outils, ...
Jetpack : collection de libairies logicielles libres (pour ne pas réeinviter la roue)
Google Play Services : libraires logicielles non-libres
NDK Android : Api pour le dév natif
# Contenu d'un projet Android
## Manifest
Contient:
- Les composants de l'app (Activités, Services, Broadcast receivers, Content providers)
- Permissions dont l'app a besoin
- Fonctionnalités hardware et software dont l'app a besoin
## Ressources
Contient le contenu statique de l'app:
- Langue et région de l'appareil
- Résolution/orientation écran
- Version android
- Images (Drawables)
- Layouts
- Animations
- Menus
- Valeurs textuelles (app_name, main_title, ...) utile pour la traduction
- Couleurs
- Themes
- ...
### Layouts
(chaque rectangle corerspond à une View)
![[Pasted image 20230923195914.png]]
#todo autres layouts que ceux de base (ConstraintLayout par ex il me semble)
![[Pasted image 20230923195922.png]]
![[Pasted image 20230923200121.png]]
#### La classe R
Contient les id des ressources de l'application
#todo et quoi d autre ?
## Code
Dans le dossier java (contient égalements les tests)
## Build scripts
Android utilise Gradle
2 fichiers gradle:
- Pour le projet complet
- Pour l'app (module appartenant au projet)
C'est également dans ce fichier que l'on met nos _dependencies_
## Config files
#question c'est quoi ???