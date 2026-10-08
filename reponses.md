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

1. commande : git revert a879970
2. revert crée un nouveau commit qui annule, et le commit d'origine reste dans l'historique
3. pourquoi c'est différent de la mission 8 : le commit était partagé, et un reset aurait réécrit un historique que les autres possèdent déjà
4. reset sert pour un historique local, revert pour un commit partagé


## Mission 11 – Correction isolée

1. commande : git cherry-pick e82ad44
2. l'id d'origine : e82ad44 (sur test/experimentations) et le nouvel id (sur main)
3. pourquoi pas un merge : il aurait aussi intégré les couleurs expérimentales et le texte de test 
4. pourquoi l'id change : c'est un nouveau commit, posé sur un autre parent

## Mission 12 – Version stable

1. 1.0.0 = MAJEURE.MINEURE.CORRECTIF
2. majeure : changements importants ou incompatibles ; mineure : nouvelles fonctionnalités compatibles ; correctif : corrections de bugs
3. correction de bug mineur : v1.0.1
4. nouvelle fonctionnalité compatible : v1.1.0
5. refonte majeure incompatible : v2.0.0


## Questions finales

1. La zone de travail contient mes fichiers en cours de modification, le staging contient ce que je prépare avec `git add`, et l'historique contient les commits enregistrés avec `git commit`.

2. Une branche permet de développer une fonctionnalité sans toucher à main, qui reste stable. On fusionne seulement quand le travail est terminé (ex : feature/services, feature/contact).

3. `git reset` (mission 8) supprime le commit et réécrit l'historique, donc à réserver à un commit local. `git revert` (mission 9) crée un nouveau commit qui annule l'ancien sans le supprimer, adapté à un commit déjà partagé.

4. Quand un travail n'est pas terminé et qu'une tâche urgente arrive : `git stash` met les modifications de côté sans commit, `git stash pop` les récupère (mission 10 avec equipe.html).

5. Le cherry-pick récupère seulement le commit voulu, alors qu'une fusion apporterait aussi les commits non prêts de la branche (mission 11 : seule la correction du titre devait aller sur main).

6. HEAD indique ma position actuelle dans l'historique, en général la branche sur laquelle je travaille.

7. HEAD~2 désigne le commit situé deux commits avant HEAD.

8. Un tag donne un nom fixe à un commit important, comme une version publiée (ex : v1.0.0).

9. Des petits commits sont plus faciles à comprendre, à annuler ou à récupérer séparément, et `git bisect` permet de retrouver plus précisément celui qui a introduit un bug.

10. Certains fichiers sont temporaires ou propres à une machine (debug.log, cache/) ou contiennent des informations sensibles (.env avec des mots de passe). On les exclut avec .gitignore.
