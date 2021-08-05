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
Visual Mode : **Touche de direction** pour selectionner et **y** pour copier
Normal Mode : **p** pour coller
- Selectionner la ligne x à y et couper
Visual Mode : **Touche de direction** pour selectionner et **d** pour couper
Normal Mode : **p** pour coller

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
- Nouveau  windows \
**:new** : Creer un nouveau  windows horizontal \
**:vnew** : Creer un nouveau  windows vertical \
```
 :e filename      - edit another file
 :split filename  - split window and load another file
 ctrl-w up arrow  - move cursor up a window
 ctrl-w ctrl-w    - move cursor to another window (cycle)
 ctrl-w_          - maximize current window
 ctrl-w=          - make all equal size
 10 ctrl-w+       - increase window size by 10 lines
 :vsplit file     - vertical split
 :sview file      - same as split, but readonly
 :hide            - close current window
 :only            - keep only this window open
 :ls              - show current buffers
 :b 2             - open buffer #2 in this window

```
See also : https://vim.rtorr.com/
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

#### Tab
https://vim.fandom.com/wiki/Using_tab_pages

### Niveau 3 : Command mapping et configuration

### Niveau 4 : Les modes
    Insert
    Normal
    Visual
    Select
    Command line
    Ex mode
    
 ### TO Be Filetered
 ```
 

Press V to switch to VISUAL LINE mode and highlight the lines you want to indent by pressing j. Then press > to indent them. So the complete command would be Vjjj>.

Alternatively, put your cursor on the <script> tag and use 4>> to indent four lines.

 -------
2662

Use the > command. To indent five lines, 5>>. To mark a block of lines and indent it, Vjj> to indent three lines (Vim only). To indent a curly-braces block, put your cursor on one of the curly braces and use >% or from anywhere inside block use >iB.

If you’re copying blocks of text around and need to align the indent of a block in its new location, use ]p instead of just p. This aligns the pasted block with the surrounding text.

Also, the shiftwidth setting allows you to control how many spaces to indent.
------
Basic commands

In normal mode, type >> to indent the current line, or << to unindent. Each command can be used with a count. The operators > and < do the same for motions, text objects and visual selections. For all commands, pressing . repeats the operation.

For example, typing 5>>.. shifts five lines to the right, and then repeats the operation twice so that the five lines are shifted three times.

In insert mode, Ctrl-T indents the current line, and Ctrl-D unindents.

When indenting or unindenting, lines are shifted one 'shiftwidth' to the right or left.
Basic examples

To adjust the indent on three lines:

    Put the cursor anywhere in the first line.
    Press V then jj to visually select the three lines.
    Press > to indent (shift text one 'shiftwidth' to the right), or press < to shift left.
    Press . to repeat the indent, or u to undo if you have shifted too far.
    Type gv if you want to reselect the lines (not needed).

Alternatively, if you know that you want to adjust three lines, you can simply:

    Type 3>> to shift right or 3<< to shift left.

Or:

    Type >2j to shift right or <2j to shift left.

As mentioned above, the > and < commands combine with arbitrary Vim movements and text objects. For example, >} to indent from the cursor to the next blank line, or <aB to un-indent the current C-like {...} "block" structure. See indent a code block.
More commands

In normal mode, type == to automatically indent the current line according to your indentation settings. This command can be used with a count. The = command does the same, but for motions, text objects and visual selections.

To reindent an entire buffer, use gg=G.

To reindent many files, the argument list can be used:


 ```
 
 ### Niveau 5 : Creation des raccourci avec map, noremap...
 https://stackoverflow.com/questions/3776117/what-is-the-difference-between-the-remap-noremap-nnoremap-and-vnoremap-mapping \
 https://vi.stackexchange.com/questions/2089/what-are-the-differences-between-the-map-noremap-abbrev-and-noreabbrev-command
