# TP 7 - TP 7 - Boot, services et processus / Tâches d’administration


## Exercice 1. Personnalisation de GRUB

#### 1. Commencez par changer l’extension du fichier /etc/default/grub.d/50-curtin-settings.cfg s’il est présent dans votre environnement (vous pouvez aussi commenter son contenu).
`mv /etc/default/grub.d/50-curtin-settings.cfg /etc/default/grub.d/50-curtin-settings.old`

#### 2. Modifiez le fichier /etc/default/grub pour que le menu de GRUB s’affiche pendant 10 secondes ; passé ce délai, le premier OS du menu doit être lancé automatiquement.
```
GRUB_DEFAULT=0
GRUB_TIMEOUT=10
GRUB_DISTRIBUTOR=`lsb_release -i -s 2> /dev/null || echo Debian`
GRUB_CMDLINE_LINUX_DEFAULT="maybe-ubiquity"
GRUB_CMDLINE_LINUX=""
GRUB_TIMEOUT_STYLE=menu
```
#### 3. Lancez la commande update-grub
Done

#### 5. On va augmenter la résolution de GRUB et de notre VM. Cherchez sur Internet le ou les paramètres à rajouter au fichier grub. 

#### 6. On va à présent ajouter un fond d’écran. Il existe un paquet en proposant quelques uns : grub2-splash-images (après installation, celles-ci sont disponibles dans /usr/share/images/grub). 

#### 7. Il est également possible de configurer des thèmes. On en trouve quelques uns dans les dépôts (grub2-themes-*). Installez-en un. 

#### 8. Ajoutez une entrée permettant d’arrêter la machine, et une autre permettant de la redémarrer. 

#### 9. Configurer GRUB pour que le clavier soit en français 

Exercice 2. Noyau Dans cet exercice, on va créer et installer un module pour le noyau. 

#### 1. Commencez par installer le paquet build-essential, qui contient tous les outils nécessaires (compilateurs, bibliothèques) à la compilation de programmes en C (entre autres). 

#### 2. Créez un fichier hello.c contenant le code suivant :








