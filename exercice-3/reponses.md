3.1 le fichier n'existe plus car les conteneurs sont éphémères, tout ce qui est créer avec le conteneur sera supprimé en même temps que le conteneur, avec l'option --rm tout a été supprimé. Chaque nouveau conteneur sera comme "neuf".

3.7 - Suppression : docker volume rm mes-donnees. Précaution : Il faut d'abord supprimer les conteneurs qui l'utilisent et s'assurer d'avoir une sauvegarde car l'action est irréversible.
