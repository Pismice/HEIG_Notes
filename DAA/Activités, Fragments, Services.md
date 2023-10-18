![[Pasted image 20231011202835.png]]
![[Pasted image 20231011224649.png]]
# Activity
- Une activité doit être déclarer comme <activity> dans le manifest avec à l'intérieur de cette 1ère <intent-filter> pour qu'elle soit lancée au début
- override fun onCreate(savedInstanceState:Bundle?) est obligatoire
- findViewById pour trouver un élément présent sur l'activity
- Définir les event dans le xml est déprécié (mais on peut toujours le voir dans certains tutos)
- Lancer une activité depuis une activité ![[Pasted image 20231011204602.png]]
- Passage de paramètres ![[Pasted image 20231011204658.png]]
- TODO: contracts

# Fragments
- Créé dans l'Activité
- Gérés par le *FragmentManager* (transistion d'états, attachement/détachement de l'Activité hôte, gestion de la pile de Fragments)
- Doivent être dans une <androidx.fragment.app.FragmentContainerView>
- supportFragmentManager pour gérer les Fragments de mon Activity
- Le fragment peut accéder à son activité via *activity*

# Services
- Opérations longues en arrière-plan
	1. Foreground: notif visible par l'utilisateur (download, lecteur audio, ...)
	2. Background: sans user interface (synchronisation, sauvegarde, ...)
	3. Bounded: Lié à une Activité (détruit lors que le composant n'est plus bindé avec lui)
- De moins en moins utilisé (Workmanager, ViewModel+LiveData de Jetpack)
- Classe qui étend Service
- #question un service doit forcement avoir un Thread ?

# Broadcast Receivers et Content Providers