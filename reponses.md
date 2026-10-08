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
