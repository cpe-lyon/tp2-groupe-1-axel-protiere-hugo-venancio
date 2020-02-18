# TP 2. Bash

## Exercice 1. Variables d'environnements

__1. Dans quels dossiers bash trouve-t-il les commandes tapées par l'utilisateur?__  
Dans les dossiers suivants :  
```bash
/usr/local/sbin    
/usr/local/bin  
/usr/sbin  
/usr/bin  
/sbin  
/bin  
/usr/games  
/usr/local/games  
/snap/bin
```
Ils sont définis par la variable d'environnement PATH  
__2. Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dans__
__votre répertoire personnel ?__  
```bash
HOME
```
__3. Explicitez le rôle des variables LANG, PWD, OLDPWD, SHELL et \_\.__  
LANG : : la variable d’environnement LANG détermine la langue que les logiciels
utilisent pour communiquer avec l’utilisateur  
PWD : Le répertoire de travail courant de l'interpréteur de commande   
OLDPWD : Le répertoire de travail courant avant la dernière commande CD    
SHELL : Donne le chemin vers l'interpréteur  
__4. Créez une variable locale MY_VAR (le contenu n’a pas d’importance). Vérifiez que la variable existe__
export VAR="abcdef" ; printenv VAR  
__5. Tapez ensuite la commande bash. Que fait-elle ? La variable MY_VAR existe-t-elle ? Expliquez. A la fin
de cette question, tapez la commande exit pour revenir dans votre session initiale.__
La commande bash ouvre un nouveau process BASH.    
Non elle n'existe pas, car ce n'est pas une variable d'environnement.  
__6. Transformez MY_VAR en une variable d’environnement et recommencez la question précédente. Expliquez.__
C'est bon ! Elle existe, car une variable d'environnement est globale donc accessible de n'importe quel processus BASH.  
__7. Créer la variable d’environnement NOMS ayant pour contenu vos noms de binômes séparés par un espace.
Afficher la valeur de NOMS pour vérifier que l’affectation est correcte.__
```bash
Export NOMS="Protiere Venancio" ; printenv NOMS
```
__8. Ecrivez une commande qui affiche ”Bonjour à vous deux, binôme1 binôme2 !” (où binôme1 et binôme2
sont vos deux noms) en utilisant la variable NOMS.__  
```bash
vim bonjour.sh
echo "Bonjour, $NOMS"
:w
:q 
. bonjour.sh
```



