# Glossaire

Les mots techniques, dans l'ordre où je les ai appris.

## Git et GitHub

**Git** — Logiciel de *gestion de versions* (version control). Il enregistre l'historique complet de mes fichiers : chaque étape est une « photo » que je peux revoir ou restaurer. Il fonctionne sur mon ordinateur, même sans Internet.

**GitHub** — Site qui héberge en ligne des projets gérés avec Git. Sert de sauvegarde, d'outil de travail à plusieurs, et de portfolio visible par les recruteurs et les clients.

**Dépôt (repository, « repo »)** — Un projet suivi par Git : le dossier de fichiers + tout son historique.

**Commit** — Une photo de l'état des fichiers à un instant donné, avec un message qui explique ce qui a changé et un auteur. L'historique d'un projet est une chaîne de commits.

**Branche (branch)** — Une ligne d'historique. La principale s'appelle en général `main`. On crée d'autres branches pour essayer quelque chose sans toucher à la version principale.

**Local / distant (remote)** — *Local* : la copie du dépôt sur la machine où je travaille. *Distant* : la copie sur GitHub. Les deux sont synchronisées à la demande, pas automatiquement.

**Push** — Envoyer mes commits locaux vers le dépôt distant (GitHub).

**Pull** — Récupérer en local les commits présents sur GitHub que je n'ai pas encore.

**Public / privé** — Un dépôt public est visible par tout le monde (utile pour un portfolio). Un dépôt privé n'est visible que par moi et les personnes que j'invite.

**README** — Le fichier d'accueil d'un dépôt. GitHub l'affiche automatiquement sous la liste des fichiers.

**Markdown (`.md`)** — Format de texte simple avec quelques symboles pour la mise en forme : `#` pour un titre, `**gras**`, `- ` pour une liste. GitHub le transforme en page lisible.

**Cloner (clone)** — Télécharger une copie complète d'un dépôt distant (fichiers + historique) sur sa machine.

**origin** — Le surnom par défaut du dépôt distant. `git push origin main` = « envoie la branche main vers origin ».

**Zone de préparation (staging area)** — L'étape entre « j'ai modifié un fichier » et « je fais un commit ». `git add` y place les fichiers choisis ; `git commit` photographie ce qu'elle contient.

**Hash** — L'empreinte unique d'un commit (ex. `f866ff3…`), calculée à partir de son contenu. Un seul caractère changé = une empreinte totalement différente.

**GitHub App** — Un programme à qui on accorde des droits précis sur des dépôts choisis, révocables à tout moment. Plus sûr que de partager son mot de passe.

**Principe du moindre privilège** — Règle de sécurité : ne donner à chacun (personne ou programme) que les droits strictement nécessaires.

**Fast-forward (avance rapide)** — Quand on fait un pull et que seul l'autre côté a avancé : Git déplace simplement ma copie jusqu'au dernier commit, sans rien fusionner.

**Conflit (merge conflict)** — Quand deux personnes ont modifié les mêmes lignes d'un fichier chacune de son côté. Git ne peut pas deviner quelle version garder, il demande à un humain de trancher.

**CLAUDE.md** — Fichier de consignes placé à la racine d'un dépôt. Claude Code le lit automatiquement au début de chaque session où le dépôt est attaché.

## Open source

**Open source** — Du code publié pour que tout le monde puisse le lire, l'utiliser et souvent le modifier, selon les conditions de sa licence.

**Licence** — Le contrat qui dit ce qu'on a le droit de faire avec un code (fichier `LICENSE` du dépôt). *MIT* et *Apache 2.0* : réutilisation libre, même commerciale, en gardant la mention de l'auteur. *GPL* : si je distribue un logiciel qui l'intègre, je dois publier mon code sous GPL aussi. **Pas de licence = tous droits réservés** : je peux lire et apprendre, pas copier.

**Star (étoile)** — Un « j'aime » sur un dépôt GitHub. Un bon indicateur de popularité, pas une garantie de qualité.

**Fork** — Ma copie personnelle du dépôt de quelqu'un d'autre, sur mon compte GitHub, que je peux modifier librement.

## Le web

**HTML** — La structure d'une page : des balises (`<div>`, `<button>`…) qui décrivent les blocs.

**CSS** — L'apparence : couleurs, tailles, mise en page. Les *variables CSS* (`--accent`) stockent une valeur réutilisée partout.

**JavaScript** — Le comportement : calculs, réactions aux clics, lecture et écriture des données.

**index.html** — Le fichier qu'un serveur web envoie par défaut quand on visite un site sans préciser de page.

**Backend** — La partie d'une application qui tourne sur un serveur (base de données, calculs cachés), par opposition au *frontend* qui tourne dans le navigateur.

## Serveurs et Internet

**VPS (Virtual Private Server)** — Un ordinateur loué dans un centre de données, allumé en permanence et joignable depuis Internet. « Virtuel » : une grosse machine physique est découpée en plusieurs machines indépendantes. J'en suis l'administratrice.

**Adresse IP** — Le numéro qui identifie une machine sur Internet (ex. `51.68.12.34`).

**Nom de domaine** — Une adresse lisible par un humain (ex. `mon-site.fr`) qu'on achète pour une durée, en général un an renouvelable.

**DNS (Domain Name System)** — L'annuaire mondial qui traduit un nom de domaine en adresse IP.
