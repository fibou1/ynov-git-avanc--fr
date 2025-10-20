# GIT TRICKS – astuces Git avancées mais pratiques

### 1. Ajouter et valider en une seule commande
```
git commit -am "message"
```
Fait `git add` et `git commit` en même temps, uniquement pour les fichiers déjà suivis par Git.

---

### 2. Modifier le message du dernier commit
```
git commit --amend -m "nouveau message"
```
Change le message du dernier commit avant de le pousser sur le dépôt distant.

---

### 3. Ajouter un fichier oublié au dernier commit
```
git add . && git commit --amend --no-edit
```
Ajoute les nouveaux fichiers au dernier commit sans modifier son message.  
À utiliser seulement si le commit n’a pas encore été poussé.

---

### 4. Sauvegarder temporairement son travail (stash)
```
git stash save "nom"
git stash list
git stash apply
```
Met de côté ton travail sans commit.  
Tu peux ensuite voir la liste des stash et les restaurer quand tu veux.

---

### 5. Afficher un historique lisible et clair
```
git log --graph --oneline --decorate
```
Affiche les commits sous forme de graphe simplifié, pratique pour comprendre les branches.

---

### 6. Supprimer les fichiers non suivis par Git
```
git clean -df
```
Efface tous les fichiers non suivis (non ajoutés à Git).  
Attention : cette commande supprime définitivement les fichiers.

---

### 7. Revenir à la branche précédente
```
git checkout -
```
Permet de revenir rapidement à la dernière branche sur laquelle tu étais.

---

### 8. Créer des alias Git utiles
À ajouter dans ton fichier `~/.bashrc` ou `~/.zshrc` :

```
alias uncommit="git reset HEAD~1"
alias recommit="git commit --amend --no-edit"
alias editcommit="git commit --amend"
```
Ces raccourcis permettent de corriger ou modifier le dernier commit rapidement.

---

### 9. Annuler les fichiers ajoutés avant commit
```
git reset .
```
Annule le `git add` sans effacer le code.  
Les fichiers repassent en “modifiés” mais non suivis.

---

### 10. Ajouter uniquement les fichiers déjà suivis
```
git add -u
```
Ajoute seulement les fichiers déjà connus par Git et modifiés.  
Les nouveaux fichiers ne seront pas pris en compte.


Ctrl + Shift + V