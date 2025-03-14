 # Workflow Git pour la gestion des User Stories

 ## 1. Se déplacer dans la branche `dev`

 Je me déplace dans la branche `dev` :
 ```bash
 git checkout dev
 ```

 ### 1.1. Mettre à jour la branche `dev` locale

 Je mets à jour ma branche `dev` locale avec la version distante :
 ```bash
 git pull
 ```
ou
```bash
git pull origin dev
 ```

 ---

 ## 2. Créer et se déplacer dans la branche de la User Story

 Je crée une nouvelle branche pour ma User Story et je m'y déplace. Si possible, je choisis une User Story qui ne va pas entrer en conflit avec celle de mon binôme pour éviter les conflits de merge.

 - Pour créer et me déplacer dans la branche :
   ```bash
   git checkout -b user_story_name
   ```

 - **Alternativement**, je peux d'abord créer la branche puis m'y déplacer :
   ```bash
   git branch user_story_name
   git checkout user_story_name
   ```

 ---

 ## 3. Travailler sur ma User Story

 Je travaille sur ma User Story et je sauvegarde régulièrement mes progrès.

 ### 3.1. Voir l'état des fichiers modifiés
 ```bash
 git status
 ```

 ### 3.2. Ajouter les fichiers à committer
 - Pour ajouter des fichiers spécifiques :
   ```bash
   git add nom_fichier1 nom_fichier2
   ```

 - Ou pour ajouter tous les fichiers modifiés :
   ```bash
   git add .
   ```

 ### 3.3. Vérifier les fichiers ajoutés
 ```bash
 git status
 ```

 ### 3.4. Faire un commit avec un message descriptif
 ```bash
 git commit -m "Mon beau message"
 ```

 ### 3.5. Vérification finale
 ```bash
 git status
 ```

 ---

 ## 4. Pousser la branche sur GitHub

 Une fois la User Story terminée, je pousse ma branche sur GitHub :
 ```bash
 git push origin user_story_name
 ```

 ---

 ## 5. Créer une Pull Request sur GitHub

 Je vais sur GitHub et crée une Pull Request (PR) de `user_story_name` vers `dev`.

 On croise les doigts pour ne pas avoir de conflits ! 🤞

 ### 5.1. Revue de code avec mon binôme
 Je review mon code avec mon binôme pour valider les changements et vérifier que tout fonctionne correctement.

 Une fois validé, on fusionne la PR et supprime la branche sur GitHub.

 **Note** : Je ne suis pas encore suffisamment à l’aise avec la gestion des conflits pour proposer une technique spécifique. La participation de tout le monde est la bienvenue pour étoffer cette section et trouver une méthode optimale !

 ---

 ## 6. Nettoyer après la PR

 ### 6.1. Revenir sur la branche `dev`
 Je me replace sur la branche `dev` :
 ```bash
 git checkout dev
 ```

 ### 6.2. Mettre à jour ma branche `dev` locale après le merge
 Je mets à jour ma branche `dev` locale après le merge effectué sur GitHub :
  ```bash
 git pull
 ```
ou
```bash
git pull origin dev
 ```

 ### 6.3. Supprimer la branche `user_story_name`
 Je supprime la branche `user_story_name` maintenant que je n'en ai plus besoin :
 ```bash
 git branch -d user_story_name
 ```

 ### 6.4. Nettoyer les branches distantes
 Je fais un `fetch` pour actualiser les branches et que Git voie que la branche distante a bien été supprimée :
 ```bash
 git fetch -p
 ```
 ### 6.5. Vérifier les branches
 Pour vérifier si j'ai bien toutes mes branches à jour en locale, je peux les lister :
 ```bash
 git branch -a
 ```

 ---

 ## 7. Prêt pour la suite !

 Tout est nettoyé, ma branche `dev` est à jour en local et en remote. Je suis prêt à repartir sur une nouvelle User Story ! 🚀
