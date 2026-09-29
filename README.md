# Rendu de AVEKOR Honoré

Une capture par étape, dans l'ordre. Terminal entier non rogné, invite visible.
Afficher l'historique en graphe quand c'est pertinent.

## Niveau 1
1. Configuration Git
![](captures/01-config.png)
2. Branche de travail
![](captures/02-branche.png)
3. Historique des commits
![](captures/03-historique.png)
4. Pull Request
![](captures/04-pull-request.png)
5. Revue croisée
![](captures/05-revue.png)

## Niveau 2
6. Secret retiré du suivi
![](captures/06-secret.png)
7. Conflit résolu (marqueurs avant, graphe après)
![](captures/07-conflit-avant.png)
![](captures/07-conflit-apres.png)
8. Revert du bandeau promo
![](captures/08-revert.png)
9. Issue fermée par une Pull Request
![](captures/09-issue.png)
10. Protection de main et CI au vert
![](captures/10-protection-pr.png)
![](captures/10-protection-ci.png)
![](captures/10-ci-verte.png)

## Cible mobile
11. Commit distant récupéré et conflit résolu
![](captures/11-mobile-conflit.png)
![](captures/11-mobile-graphe.png)

## Trois commits annotés
1. `5a8f491` : retire config/secrets.env du suivi avec git rm --cached et l'ajoute au .gitignore. Le fichier reste en local mais ne peut plus être commité. Le mot de passe reste lisible dans l'historique (ff28a3f), il doit donc être considéré comme compromis et changé.
2. `4796181` : merge de feature/couleurs dans feature/titre. Les deux branches modifiaient la même ligne h1 ; la résolution garde le texte de l'une et la classe hero de l'autre.
3. `8e521d4` : git revert du commit a35a690 (bandeau promo). Le revert crée un nouveau commit qui annule l'ancien sans réécrire l'historique, contrairement à reset, ce qui est indispensable sur une branche main protégée et partagée.