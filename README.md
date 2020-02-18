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
__9. Quelle différence y a-t-il entre donner une valeur vide à une variable et l’utilisation de la commande
unset ?__  
Si on donne une valeur vide, la variable existera quand même mais sera vide. Si on utilise unset, la variable sera undefined, donc elle n'exisetera même plus.  
  
__10. Utilisez la commande echo pour écrire exactement la phrase : $HOME = chemin (où chemin est votre
dossier personnel d’après bash)__
```bash
vim homedir.sh
echo '$HOME =' $HOME
:w
:q 
. homedir.sh
```
### Programmation Bash
__Vous enregistrerez vos scripts dans un dossier script que vous créerez dans votre répertoire personnel.
Tous les scripts sont bien entendu à tester.__  
__Ajoutez le chemin vers script à votre PATH de manière permanente.__  
```bash
"PATH=$PATH:~/script"
```
## Exercice 2. Contrôle de mot de passe
__Écrivez un script testpwd.sh qui demande de saisir un mot de passe et vérifie s’il correspond ou non au
contenu d’une variable PASSWORD dont le contenu est codé en dur dans le script. Le mot de passe saisi par
l’utilisateur ne doit pas s’afficher.__  
  
## Exercice 3. Expressions rationnelles
__Ecrivez un script qui prend un paramètre et utilise la fonction suivante pour vérifier que ce paramètre
est un nombre réel :__
```bash
function is_number()
{
    re='^[+-]?[0-9]+([.][0-9]+)?$'
    if ! [[ $1 =~ $re ]] ; then
        return 1
    else
        return 0
    fi
}
```
__Il affichera un message d’erreur dans le cas contraire.__  
  
## Exercice 4. Contrôle d’utilisateur
__Écrivez un script qui vérifie l’existence d’un utilisateur dont le nom est donné en paramètre du script. Si le
script est appelé sans nom d’utilisateur, il affiche le message : ”Utilisation : nom_du_script nom_utilisateur”,
où nom_du_script est le nom de votre script récupéré automatiquement (si vous changez le nom de votre
script, le message doit changer automatiquement)__  
  
## Exercice 5. Factorielle
__Écrivez un programme qui calcule la factorielle d’un entier naturel passé en paramètre (on supposera que
l’utilisateur saisit toujours un entier naturel).__  
  
## Exercice 6. Le juste prix
__Écrivez un script qui génère un nombre aléatoire entre 1 et 1000 et demande à l’utilisateur de le deviner.
Le programme écrira ”C’est plus !”, ”C’est moins !” ou ”Gagné !” selon les cas (vous utiliserez $RANDOM).__  
  
## Exercice 7. Statistiques
__1. Écrivez un script qui prend en paramètres trois entiers (entre -100 et +100) et affiche le min, le max
et la moyenne. Vous pouvez réutiliser la fonction de l’exercice 3 pour vous assurer que les paramètres
sont bien des entiers.__  
  
__2. Généralisez le programme à un nombre quelconque de paramètres (pensez à SHIFT)__  
  
__3. Modifiez votre programme pour que les notes ne soient plus données en paramètres, mais saisies et
stockées au fur et à mesure dans un tableau.__  
  
## Exercice 8. Pour les plus rapides
__Écrivez un script qui affiche les combinaisons possibles de couleurs (cf. TP 1) :__  
  



