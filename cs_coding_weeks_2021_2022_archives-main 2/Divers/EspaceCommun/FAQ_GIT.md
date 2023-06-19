# FAQ GIT Coding Weeks 
## par les 3A INFONUM 2020-2021


### Travailler ensemble sur du code
On utilise un outil de version control (gestionnaire de version) comme Git (voir [Wtf is Git]() ), de pairavec un service de hosting pour ce version control (hébergement en ligne des fichiers) comme GitLabou GitHub.


#### Wtf is Git

Git est un outil très utile pour coder en groupe. Il fait office de
* **Communication avec un repo central** : le repo (dossier) central est distant (hébergé en ligne),souvent sur un site comme GitHub ou GitLab. Le repo central distant sert de référence pourtous les développeurs : quand on veut modifier des fichiers dans le projet, on pull (récupère)le repo distant (qui est le plus à jour), on fait ses modifications, puis on push (envoie) vers lerepo distant pour le tenir à jour.* **Gestionnaire de version** (on peut consulter l'historique de version des différents codes dechaque personne qui contribue au projet). Exemple : Alice veut changer le schéma decouleurs de son jeu 2048. Elle se dit que des nuances de bleu, c'est pas mal. Elle change enbleu, fait un commit avec comme message "now in blue (first test)" et push vers le repodistant. Après discussion avec son client, il voulait plutôt du vert. Elle change donc en vert,commit avec "now in green after client feedback", et push vers le repo distant. Elle auratoujours accès aux versions précédentes, si elle a besoin de revenir en arrière, ou d'expliquerà Bob le stagiaire qui vient d'arriver pourquoi on est en vert et pas bleu : l'explication dechaque version est dans le message du commit.
* **Merger intelligent** : Git est capable de faire une fusion automatique entre les fichiers, engardant les bonnes infos (la plupart du temps). Exemple : Alice pull le repo distant pourchanger le schéma de couleurs de son jeu 2048. Bob pull le repo distant pour changer lapolice de caractère utilisée dans le jeu. Alice finit avant Bob (trop forte) et push son travail surle repo distant. Bob finit un peu plus tard, se rend compte qu'il n'a pas la dernière version(celle d'Alice) et fait un nouveau pull. Git s'occupe d'intégrer le code d'Alice dans le repo localde Bob sans casser le code de Bob. Il est satisfait, et peut push, mettant le repo distant à jour.* **Branching** : Git propose un système de branches, ce qui permet de travailler sur des featuressans se marcher sur les pieds. Ex : Alice et Charlie veulent changer les couleurs du jeu. Bobtravaille toujours en parallèle sur la police de caractère. Alice et Charles ont besoind'échanger régulièrement et de se débeuguer l'un l'autre ; l'écran d'Alice n'affiche que du bleu,et Charlie est daltonien. Pour ne pas mettre sur la branche "master" qui est la référence, et nepas polluer le travail de Bob avec des allers retours sur les teintes de rouge, ils vont travaillersur une nouvelle branche, qu'ils nomment colorBranch. Alice se place sur la branchecolorBranch (en local) et travaille. Quand elle push, ce sera bien vers le repo distant, mais surla branche distante colorBranch (pas master). Charlie pourra ainsi pull depuis le repo distantde la branche colorBranch, vers sa propre branche colorBranch locale. Quand il aura fini, ilpush vers colorBranch (du repo distant) etc. Tant qu'ils débeuguent encore, Bob ne verra pasleur travail sur la branche master, et ne sera pas pollué par leurs " #TODO" et "#ICI ÇA NEMARCHE PAS". Quand ils ont fini de débeuguer, Alice nettoiera le code, puis ouvrira uneMerge Request (demande de fusion) de la branche distante colorBranch dans le branchedistante master. GitLab s'occupe alors de fusionner automatiquement les 2 branches, ce quiincorpore le travail d'Alice et Charlie dans la branche master, sans casser le travail de Bob.


#### Setup un repo Gitlab pour travailler ensemble

* Chaque personne se [connecte au Gitlab de l'école]().
* Si on choisit d'utiliser le protocole ssh (plutôt que https) : Chaque personne ajoute une clé sshà son compte gitlab. Voir Gitlab avec une clé SSH
* Une seule personne crée le repo GitLab. Voir Créer un nouveau repo sur GitLab
* Cette même personne invite les autres membres du groupe. Voir Inviter les copains àtravailler sur votre repo Git
* Une fois que tout le monde est maintainer, tout le monde clone le repo sur sa machine (voirCloner un repo git )
* Tout le monde se place dans le repo fraîchement cloné (voir Cheatsheet bash )*  Une fois que tout le monde a un clone du repo en local (donc sur sa propre machine), tout lemonde fait un commit initial (voir Initial commit ou apprendre vos commandes git préférées )avec un petit changement pour tester que le setup est bon.


### Connexion au Gitlab
* Connexion à Gitlab : Il faut le lien vers le domaine GitLab que vous allez utiliser. Pour les CodingWeeks 2021, c'est `https://gitlab-ovh-XX.cloud.centralesupelec.fr/`
* Choisir l'onglet "LDAP CS"
* Identifiant : mail cs (c'est l'identifiant long pour les services de l'école)
* Mot de passe : votre mdp du CAS CS (c'est probablement votre mot de passe Géode ou Edunao)



### Gitlab avec une clé SSH

Voir [ce tuto](ssh.md).


### Créer un nouveau repo sur GitLab


Sur la page d'accueil : "New Project"


### Inviter les copains à travailler sur votre repo Git
