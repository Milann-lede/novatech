# Compte rendu – TP final Git NovaTech

## Mission 5 – Analyse du projet
1. Identifiant court du premier commit : d034632 (Création de la page d'accueil)
2. Commit correspondant à l'ajout de la page Contact : c9eb5c2 (Création de la page Contact)
3. Nombre de commits à ce stade : 6
4. Commande pour afficher l'historique graphique : git log --oneline --graph --all

Commande utilisée pour examiner un commit Contact : git show c9eb5c2


## Mission 8 – Commit local incorrect


1. commande utilisée : git reset --mixed HEAD~1
2. reset fait reculer la branche d'un commit, et le mode mixed annule le commit et vide le staging sans toucher au contenu des fichiers
3. méthode qui aurait tout supprimé : git reset --hard HEAD~1


## Mission 9 – Commit partagé à annuler

1. commande : git revert <id>
2. revert crée un nouveau commit qui annule, et le commit d'origine reste dans l'historique
3. pourquoi c'est différent de la mission 8 : le commit était partagé, et un reset aurait réécrit un historique que les autres possèdent déjà
4. reset sert pour un historique local, revert pour un commit partagé


## Mission 11 – Correction isolée

1. commande : git cherry-pick <id>
2. l'id d'origine (sur test/experimentations) et le nouvel id (sur main)
3. pourquoi pas un merge : il aurait aussi intégré les couleurs expérimentales et le texte de test 
4. pourquoi l'id change : c'est un nouveau commit, posé sur un autre parent