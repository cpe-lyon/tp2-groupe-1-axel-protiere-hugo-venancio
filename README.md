# TP 2. Bash

## Exercice 1. Variables d'environnements

__1. Dans quels dossiers bash trouve-t-il les commandes tapées par l'utilisateur?__ 
Dans les dossiers suivants :  
/usr/local/sbin    
/usr/local/bin  
/usr/sbin  
/usr/bin  
/sbin  
/bin  
/usr/games  
/usr/local/games  
/snap/bin  
Ils sont définis par la variable d'environnement PATH  
__2. Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dans__
__votre répertoire personnel ?__  
HOME      
__3. Explicitez le rôle des variables LANG, PWD, OLDPWD, SHELL et _.__  
LANG : : la variable d’environnement LANG détermine la langue que les logiciels
utilisent pour communiquer avec l’utilisateur  
PWD : Le répertoire de travail courant de l'interpréteur de commande   
OLDPWD : Le répertoire de travail courant avant la dernière commande CD    
SHELL : Donne le chemin vers l'interpréteur  
__4. Créez une variable locale MY_VAR (le contenu n’a pas d’importance). Vérifiez que la variable existe__
export VAR="abcdef" ; printenv VAR
5. 

