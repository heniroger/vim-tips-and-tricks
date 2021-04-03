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

- Aller au debut du fichier \
Normal mode : **gg** ou **1G** 
- Aller à la fin du fichier \
Normal mode : **G** 
- Retourner à la ligne precédent \
Normal mode : **CTRL+O** ou **CTRL+I** (CTRL+I pour le window precedent) \
Une autre astuce : \
Normal mode : **mx** : Marquer tout d'abord la ligne que vous voulez retourner et après cela, allez à n'importe quel ligne. \
Normal mode : **'x** : Retouner à la ligne que vous avez marqué precedemment \
Normal mode : **backquote+x**(ALTGR+7 et x) : Retouner à la ligne que vous avez marqué precedemment à l'emplacement exacte du curseur

- Retourner à la ligne edité precedent et suivant \
Normal mode : **g;** : modification precedent\
Normal mode : **g,** modification suivant
- Aller à la ligne x du fichier \
Normal mode : **5G** : Aller à la ligne 5(5 est variable selon la ligne exisant) 

- Aller au debut de la ligne \
Normal mode : **0** \
Normal mode : **^** (s'il y a un espace vide au debut de la ligne [espace ou tab] aller au debut premier mot ) \
Normal mode : **_** (s'il y a un espace vide au debut de la ligne [espace ou tab] aller au debut premier mot )

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

- Avancer/Reculer de Phrase par phrase \
Normal mode : **(** : Reculer \
Normal mode : **)**  : Avancer 

- Avancer/Reculer de Paragraphe par paragraphe \
Normal mode : **{** : Reculer \
Normal mode : **}**  : Avancer

- Copier la ligne \
Normal mode : **yy** : y comme yank \
Normal mode : **y%** ?????????
- Copier le mot \
Normal mode : **yiw**
- Copier les mots de x à y \
Normal mode : **3yy** : Copier 3 lignes \
Normal mode : **y^** : Copier depuis le curseur jusqu'au debut de la ligne \
Normal mode : **y$** : Copier depuis le curseur jusqu'à la fin de la ligne
- Couper la ligne
Normal mode : **dd** \
- Couper le mot \
Normal mode : **diw**
- Couper les mots de x à y \
Normal mode : **3dd** : Couper 3 lignes  \
Normal mode : **d^** : Couper depuis le curseur jusqu'au debut de la ligne \
Normal mode : **d$** : Coupier depuis le curseur jusqu'à la fin de la ligne
- Coller \
Normal mode : **p** :

- Selectionner la ligne x à y et copier
- Selectionner la ligne x à y et couper
- Selectionner la ligne xa à xb et copier
- Selectionner la ligne xa à xb et couper
- Selectionner la ligne xa à xb et entoure de accolade/quote/double quote/parenthese
- Rechercher
- Rechercher et Remplacer un mot
- Rechercher et remplacer tout
- Lancer un commande externe

- Autres commande \
Normal mode : **''** \
Normal mode : **backquote+backquote** \
Normal mode : **'.** \
Normal mode : **%** \
Normal mode : **|** \
Normal mode : **15|** 

### Niveau 2 : Buffer, Window, Tab
- **Un ou plusieurs windows** peut afficher **un seul buffer**( ~fichier~ ).
- **Un buffer**  peut etre **detacher des windows**
- **Un tab** peut contenir **un à plusieurs windows**

#### Windows
- Nouveau  windows 
**:new** : Creer un nouveau  windows horizontal \
**:vnew** : Creer un nouveau  windows vertical \
#### Buffer 
- Nouveau buffer \
**:edit path_fichier**  ou **:e path_fichier** : Ouvrir un fichier et automatiquement ***Créer un nouveau buffer*** \
Note : Lorsque vous editer un fichier, vous devez enregistrer pour editer un autre fichier. \
Si vous ne voulez pas cela,vous pouvez le desactiver par cette commande  **:set hidden** 
- Lister buffer \
**:buffers** ou **:ls** 
- Indicateur dans la liste des buffers
```
1  h    "fichier1.txt"   Line 1 
2  %a   "fichier2.txt"   Line 14
3  h    "fichier3.txt"   Line 10
4  #h   "fichier4.txt"   Line 1
```
**1** :  Buffer numero 1 \
**%** : *current*, Buffer dans Windows courant \
**a** : *active*, Etat de buffer : active et charger dans windows \
**h** : *hidden*, Etat de buffer : caché \
**#** : *alternate* Buffer chargé au dessous de Buffer dans Windows courant.
- Naviguer sur les buffers \
**:buffer N** ou **:b N** : Exemple :buffer 5 , Acceder au buffer numero 5 \
**:bnext** ou **:bn** : Afficher le buffer suivant \
**:bprevious** ou **:bp** : Afficher le  buffer precedent \
**:bfirst** ou **:bf** : Afficher le premier buffer \
**:blast** ou **:bl** : Afficher le dernier buffer \
**:ball** ou **:b a** : Afficher tous les buffers 
- Suppression buffer
**:bdelete arg** ou **:bd arg** supprimer un buffer avec *arg* passer en parametre. *arg* peut etre **aucun ou un ou plusiers numero du buffer ou nom fichier**  \
Exemple : *:bd* , *:bd 1 2 3* , *:bd test1.txt test2.txt* \
**:1,3bd** : Supprimer les buffers numero 1 jusqu'au numero 3


### Niveau 3 : Command mapping et configuration

### Niveau 4 : Les modes
    Insert
    Normal
    Visual
    Select
    Command line
    Ex mode
