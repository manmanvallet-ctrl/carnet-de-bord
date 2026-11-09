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

**Diff** — La vue « avant / après » d'un commit : lignes retirées en rouge, ajoutées en vert. L'outil n°1 pour relire un changement.

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

**Tableau (array)** — Une liste de valeurs entre crochets en JavaScript, ex. `["rose","bleu"]`. Le code peut la parcourir élément par élément.

**Hexadécimal (couleur)** — Une couleur écrite `#RRVVBB` : deux chiffres de 00 à ff pour le rouge, le vert et le bleu. Ex. `#1f8a4c`.

**localStorage** — Un petit espace de stockage dans le navigateur. Les données restent sur cet appareil, dans ce navigateur, et disparaissent si on efface les données du site.

**Debounce** — Attendre un court instant (ici 350 ms) avant d'enregistrer, pour ne pas écrire à chaque frappe. Il faut penser à tout enregistrer quand on quitte la page.

**Modèle de données** — La façon dont l'information est organisée (ex. une poche d'épargne = un nom, un bénéficiaire, des sources avec leur montant). Tout le reste du code en dépend.

**Migration** — Du code qui convertit les données existantes vers un nouveau modèle de données, pour qu'une mise à jour ne casse rien.

**Adaptateur (adapter)** — Un morceau de code qui imite une interface existante (ici la base de l'artefact) pour en remplacer une autre (le localStorage) sans toucher au reste du code.

**Production / développement** — *Production* : la version utilisée pour de vrai, avec les vraies données. *Développement* : une copie sur laquelle on peut tout casser sans risque.

**Test automatisé** — Un script qui utilise l'appli comme un humain (ouvrir, cliquer, vérifier) et signale les erreurs. Ici avec **Playwright**, qui pilote un navigateur sans fenêtre (*headless*).

**Backend** — La partie d'une application qui tourne sur un serveur (base de données, calculs cachés), par opposition au *frontend* qui tourne dans le navigateur.

**Frontend** — La partie d'une application qui tourne dans le navigateur : écrans, boutons, calculs affichés.

**API** — Le guichet par lequel un programme demande un service à un autre (ex. l'appli demande une analyse à une IA).

**Clé d'API** — Le badge qui identifie et facture celui qui appelle une API. Elle doit rester sur un serveur, jamais dans le code d'une page.

**Authentification / autorisation** — *Authentification* : prouver qui on est (identifiant, mot de passe). *Autorisation* : décider ce que chacun a le droit de voir ou faire.

**Local-first** — Une architecture où les données vivent d'abord sur l'appareil, puis se synchronisent avec un serveur (ex. Actual Budget). C'est notre plan V1 → V2.

**Agrégation bancaire (DSP2)** — Récupérer automatiquement ses opérations bancaires, avec son accord, via un prestataire agréé. Encadré en Europe par la directive DSP2.

**Prompt système** — Les instructions permanentes données à une IA pour fixer son rôle et son ton (ex. « bienveillant mais exigeant, sans être niais »).

## Développement (9 novembre)

**Framework** — Une boîte à outils toute prête pour construire une appli (React, Vue…). On a choisi de s'en passer pour l'instant, pour comprendre chaque ligne.

**Module (import / export)** — Un fichier JavaScript qui a un rôle précis et n'expose que ce qui sert aux autres (`export`) ; les autres fichiers le récupèrent avec `import`.

**Séparation des responsabilités** — Chaque partie du code fait une seule chose : les calculs d'un côté, l'affichage de l'autre, l'enregistrement ailleurs.

**Fonction pure** — Une fonction qui calcule un résultat à partir de ce qu'on lui donne, sans rien lire ni modifier ailleurs. Facile à tester.

**Test unitaire** — Un petit programme qui vérifie qu'une fonction donne le bon résultat sur des cas connus (`node --test`).

**Test de bout en bout (end-to-end)** — Un robot qui utilise l'appli dans un vrai navigateur, comme une personne, et vérifie chaque étape.

**Asynchrone** — Qui se produit « juste après » et non immédiatement (ex. le changement d'écran après un clic). Un test qui n'attend pas tombe dans une **race condition** (une « course »).

**Sélecteur CSS** — La partie d'une règle CSS qui dit à quels éléments elle s'applique (`.cat > input + span`). Trop large, il touche des éléments imprévus.

**Toast** — Un message bref qui apparaît en bas de l'écran puis disparaît seul (« Dépense enregistrée · Annuler »).

**Espace insécable** — Une espace qui empêche de couper la ligne entre deux mots (« 86 € »). Invisible, mais différente d'une espace normale pour un ordinateur.

**Constante nommée** — Une valeur fixe rangée à un seul endroit sous un nom explicite (`JOUR_PROJECTION_FIABLE = 5`), plutôt qu'écrite en dur partout.

**DRY (Don't Repeat Yourself)** — Ne pas copier deux fois le même code : on le range à un endroit et on le réutilise.

**Langage commun (ubiquitous language)** — Un mot par notion, le même dans le code et à l'écran.

**Feedback (retour utilisateur)** — Ce que dit une vraie utilisatrice en se servant du produit : indispensable, même quand tous les tests passent.

**Onboarding progressif** — Poser le minimum de questions au départ, puis les autres au moment où elles servent.

## Conception produit

**Discovery (phase de découverte)** — Comprendre le problème à résoudre avant de construire, par des questions, de l'observation, des chiffres.

**Spécification** — La description précise de ce qu'on veut : quoi, où, pour qui, quel résultat attendu.

**Product owner (chef de produit)** — La personne qui décide de ce qu'on construit et dans quel ordre, et qui valide le résultat.

**User story (récit utilisateur)** — Un besoin écrit sous la forme « En tant que…, je veux…, afin de… ».

**MoSCoW** — Une méthode de priorisation : *Must have* (indispensable), *Should have* (important), *Could have* (bonus), *Won't have* (pas maintenant).

**MVP (Minimum Viable Product)** — La plus petite version utile d'un produit, livrée vite pour apprendre des retours.

**Feuille de route produit (roadmap)** — Le découpage d'un produit en versions successives, chacune utilisable seule.

**Persona** — Le profil type d'utilisateur pour qui on conçoit (ici : Damien, qui fuit le sujet de l'argent).

**Wireframe / maquette / prototype** — Une représentation des écrans avant le code. *Prototype cliquable* : une maquette où les boutons fonctionnent.

**Parcours utilisateur (user flow)** — L'enchaînement d'étapes pour accomplir une tâche (ex. créer un projet en 3 étapes).

**Architecture de l'information** — La façon dont les écrans et les contenus sont découpés et reliés entre eux.

**UX (expérience utilisateur)** — Tout ce que ressent l'utilisateur en se servant d'un produit : facilité, clarté, plaisir.

**UX writing** — La rédaction des textes d'une interface. Un bon libellé dit à l'utilisateur ce qu'il doit faire, sans jargon.

**Mobile first** — Concevoir d'abord pour le téléphone, puis adapter au grand écran.

**Gestion par exception** — Traiter automatiquement ce qui est sûr et ne montrer à l'humain que ce qui demande une décision.

**Réconciliation (rapprochement)** — Comparer deux sources de données (ses saisies et le relevé bancaire) pour repérer les écarts.

**Benchmark** — L'analyse de ce que font les concurrents, pour confirmer ses choix, emprunter des idées et se différencier.

## Finances personnelles

**Agios** — Les intérêts et frais que la banque facture quand on est à découvert.

**Épargne de précaution (matelas de sécurité)** — De l'argent disponible tout de suite pour absorber un imprévu, souvent 3 à 6 mois de dépenses.

**Effet boule de neige** — Rembourser une dette fait baisser les intérêts, et l'argent économisé accélère le remboursement suivant.

**Enveloppe** — Une somme mise de côté pour un usage précis (cadeaux, plaisir).

**Provision** — Mettre de côté chaque mois 1/12 d'une dépense annuelle (taxe foncière, rentrée).

**Budget base zéro** — Chaque euro reçoit une mission : à la fin, aucun euro sans affectation.

**Jours d'avance** — Combien de jours de dépenses l'argent déjà sur le compte peut couvrir. Négatif = on vit sur le découvert.

**CIF / AMF** — En France, donner des conseils d'investissement personnalisés exige un statut (CIF, conseiller en investissement financier), contrôlé par l'AMF (Autorité des marchés financiers).

## Serveurs et Internet

**VPS (Virtual Private Server)** — Un ordinateur loué dans un centre de données, allumé en permanence et joignable depuis Internet. « Virtuel » : une grosse machine physique est découpée en plusieurs machines indépendantes. J'en suis l'administratrice.

**Adresse IP** — Le numéro qui identifie une machine sur Internet (ex. `51.68.12.34`).

**Nom de domaine** — Une adresse lisible par un humain (ex. `mon-site.fr`) qu'on achète pour une durée, en général un an renouvelable.

**DNS (Domain Name System)** — L'annuaire mondial qui traduit un nom de domaine en adresse IP.
