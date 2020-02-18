# TP 2. Bash

## Exercice 1. Variables d'environnements

1. __Dans quels dossiers bash trouve-t-il les commandes tapées par l'utilisateur?   
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
2. __Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dans
__votre répertoire personnel ?__
HOME   
3. __Explicitez le rôle des variables LANG, PWD, OLDPWD, SHELL et _. 
LANG : : la variable d’environnement LANG détermine la langue que les logiciels
utilisent pour communiquer avec l’utilisateur  
PWD : Le répertoire de travail courant de l'interpréteur de commande   
OLDPWD : Le répertoire de travail courant avant la dernière commande CD    
SHELL : Donne le chemin vers l'interpréteur  
4. __Créez une variable locale MY_VAR (le contenu n’a pas d’importance). Vérifiez que la variable existe
export VAR="abcdef" ; printenv VAR
5. 

