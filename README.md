# TP 7 - TP 7 - Boot, services et processus / Tâches d’administration


## Exercice 1. Personnalisation de GRUB

#### 1. Commencez par changer l’extension du fichier /etc/default/grub.d/50-curtin-settings.cfg s’il est présent dans votre environnement (vous pouvez aussi commenter son contenu).
`mv /etc/default/grub.d/50-curtin-settings.cfg /etc/default/grub.d/50-curtin-settings.old`

#### 2. Modifiez le fichier /etc/default/grub pour que le menu de GRUB s’affiche pendant 10 secondes ; passé ce délai, le premier OS du menu doit être lancé automatiquement.
