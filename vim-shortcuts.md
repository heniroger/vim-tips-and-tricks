# RACCOURCIS VIM 

## Raccourcis minimaux à maitriser

### Niveau 1 : Commande de base
- Changement de mode
  - Normal -> Insert : **i**
  - Insert -> Normal : **Esc** ou **CapsLock**
  - Normal -> Visual : **v**
  - Visual -> Normal : **Esc** ou **CapsLock**
- Deplacement (Normale mode) 
  - **h** : Gauche
  - **j** : Bas
  - **k** : Haut
  - **l** : Droite
  
- Annuler ~(CTRL+Z)~ \
Normal mode : **u** comme  **undo** et **CTRL+R** pour **redo**
- Enregistrer \
Normal mode : **:w**
- Quitter 
  - Quitter et enregistrer \
Normal mode : **:wq**

  - Quitter et sans enregistrer \
Normal mode : **:q!**
  - Quitter si aucune modification \
Normal mode : **:q**

- Aller au debut du fichier  
- Aller à la fin du fichier
- Retourner à la ligne precédent
- Aller à la ligne x et retourner à ligne y
- Aller au debut de la ligne \
Normal mode : **0** \
Normal mode : **^** (s'il y a un espace vide au debut de la ligne [espace ou tab] aller au debut premier mot )
- Aller à la fin de la ligne \
Normal mode : **$** \
Normal mode : **g_** (s'il y a un espace vide à la fin de la ligne [espace ou tab] aller à la fin dernier mot )
- Aller au debut du mot suivant \
Insert mode : **CTRL+RIGHT** \
Normal mode : **w**  (On peut ajouter des chiffres [**xw**] comme **3w** pour avancer de **3 mots**)
- Aller au debut du mot precédent \
Insert mode : **CTRL+LEFT** \
Normal mode : **b** (On peut ajouter des chiffres [**xb**] comme **3b** pour reculer de **3 mots**)
- Aller à la fin du mot \
Normal mode : **e** (On peut ajouter des chiffres [**xe**] comme **3e** pour avancer de **3 mots**)
- Copier la ligne
- Copier le mot
- Copier les mots de x à y
- Couper la ligne
- Couper le mot
- Couper les mots de x à y
- Coller 
- Selectionner la ligne x à y et copier
- Selectionner la ligne x à y et couper
- Selectionner la ligne xa à xb et copier
- Selectionner la ligne xa à xb et couper
- Selectionner la ligne xa à xb et entoure de accolade/quote/double quote/parenthese
- Rechercher
- Rechercher et Remplacer un mot
- Rechercher et remplacer tout
- Lancer un commande externe
### Niveau 2 : Buffer, Window, Tab

