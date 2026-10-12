# RoomWordSample

Application Java du tutoriel **Android Room with a View**. Elle affiche une liste de mots stockée localement avec Room. La base est observée avec LiveData; l'interface utilise un ViewModel, un Repository et une RecyclerView. Le bouton « + » ouvre une activité qui renvoie le nouveau mot à l'écran principal.

## Ouvrir et lancer

1. Ouvrir ce dossier dans Android Studio.
2. Laisser Gradle synchroniser les dépendances.
3. Créer ou choisir un émulateur Android (API 23 ou plus) ou brancher un appareil.
4. Lancer la configuration `app`.

Au premier lancement, la liste commence avec « Hello » et « World ». Ajouter un mot avec « + », puis relancer l'application pour constater que les données restent dans la base locale.

## Classes principales

- `Word` décrit une ligne de la table Room `word_table`.
- `WordDao` contient l'insertion et la requête alphabétique observée par LiveData.
- `WordRoomDatabase` construit la base singleton et ajoute les deux mots initiaux.
- `WordRepository` exécute les écritures en arrière-plan.
- `WordViewModel` fournit les mots à l'interface.
- `MainActivity` observe la liste et ouvre `NewWordActivity`.
- `WordListAdapter` et `WordViewHolder` affichent chaque mot.

## Correspondance au tutoriel

Le codelab lié à l'exercice est déprécié. Cette implémentation conserve ses étapes et ses concepts (Room, DAO, LiveData, Repository, ViewModel, RecyclerView et activité de saisie), avec les versions stables récentes des dépendances. `ActivityResultLauncher` remplace l'ancienne API `startActivityForResult` utilisée dans le texte du codelab.
