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

**Donnée dérivée** — Une valeur qu'on recalcule à partir d'autres données (le solde = versements − dépenses) plutôt que de l'enregistrer : toujours juste.

**Placeholder** — Le texte d'exemple grisé dans un champ vide (« Ex. week-end à la mer ») : ce n'est pas une vraie valeur.

**Onboarding progressif** — Poser le minimum de questions au départ, puis les autres au moment où elles servent.

**Simulation (modèle)** — Un calcul qui rejoue l'avenir mois par mois à partir d'hypothèses (trou, agios, effort) pour donner une date. Un modèle simplifie la réalité : ici, on suppose les agios proportionnels au découvert, alors qu'une partie sont des frais fixes.

**Route (sous-écran)** — Un écran repéré par la fin de l'adresse (`#plan`). Le navigateur la retient : le bouton « retour » fonctionne et on peut ouvrir l'écran directement.

**Paramètre d'entrée / sortie** — Ce qu'on donne à une fonction (le trou, les agios, l'effort) et ce qu'elle rend (le nombre de mois, la date, le mois par mois).

**Cas limite (edge case)** — Une situation au bord des règles normales : effort à 0 €, trou déjà rebouché, 0 € d'agios. C'est là que se cachent les bugs, donc là qu'on teste en priorité.

**Variable CSS locale** — Une variable CSS posée sur un seul élément (`style="--zero:40%"`) pour que la feuille de style s'en serve : ici, la place du zéro sur la jauge.

**Affordance** — La capacité d'un écran à montrer de lui-même ce qu'on peut y faire. Une fonction cachée derrière un lien a une mauvaise affordance.

**Période (cycle)** — Un intervalle de dates avec un début compris et une fin non comprise (du 28 octobre inclus au 28 novembre exclu). Le mois de paie n'est pas forcément le mois du calendrier.

**Événement tactile (touchstart / touchend)** — Le signal que le navigateur envoie quand un doigt se pose sur l'écran, puis se lève. En comparant les deux positions, on reconnaît un balayage (swipe) : surtout horizontal et assez long.

**Animation CSS (@keyframes)** — Une petite transition décrite dans la feuille de style : ici, le nouvel écran arrive en glissant de 40 pixels. Elle est désactivée si le téléphone demande moins d'animations (accessibilité).

**optgroup** — Dans une liste déroulante HTML, un titre qui regroupe des choix (« Dépenses régulières », « Épargne »).

**aria-pressed** — Un attribut d'accessibilité qui dit aux lecteurs d'écran qu'un bouton est « enfoncé » (le montant choisi parmi les pastilles).

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

## Agents et outils d'IA (10 novembre)

**Skill (compétence d'agent)** — Un dossier de consignes et de scripts qu'on installe dans un agent de code. L'agent le charge quand la tâche correspond : c'est une façon de lui transmettre un savoir-faire réutilisable, au lieu de tout réexpliquer à chaque fois. Taste Skill (10/11) et UI UX Pro Max (23/11) en sont deux exemples.

**Hook** — Un script que l'outil lance tout seul à un moment précis (par exemple à la fin de chaque réponse). Puissant, donc à lire avant d'installer : il s'exécute sans qu'on le demande.

**Proxy** — Un intermédiaire par lequel passent les connexions sortantes d'une machine. Il peut autoriser ou refuser un site : c'est lui qui bloquait Wikimedia pendant l'essai.

**Site vitrine** — Un site qui présente une activité (qui, quoi, où, horaires, prix) sans être un outil : on le lit, on ne s'en sert pas comme d'une appli.

**Linter** — Un programme qui relit du code ou du texte et signale les défauts selon des règles fixes. Il ne comprend pas le sens : celui de la skill ne connaît que les mots anglais.

**WebP** — Un format d'image plus léger que le JPEG à qualité égale. Chaque fichier commence par un en-tête qui annonce sa taille ; s'il est faux, le navigateur refuse l'image.
**Zone DNS** — La fiche d'un nom de domaine dans l'annuaire : la liste de ses enregistrements. On la modifie chez le vendeur du domaine (OVH).

**Enregistrement A / AAAA** — « Ce nom correspond à cette adresse IP ». A pour les adresses classiques (IPv4, `185.199.108.153`), AAAA pour les plus récentes et plus longues (IPv6, `2606:50c0:8000::153`).

**CNAME** — Un alias : « `www` est la même chose que telle autre adresse, va demander là-bas ». Il ne peut pas cohabiter avec un autre enregistrement sur le même nom.

**MX** — « Le courrier de ce domaine se livre à tel serveur ». Sans lui, la boîte `contact@` ne reçoit rien.

**TXT** — Un enregistrement qui contient juste du texte. Il ne dirige personne : il sert de preuve (« ce domaine est à moi », pour GitHub ou Google) ou de consigne (SPF).

**SPF (Sender Policy Framework)** — Un TXT qui dit quels serveurs ont le droit d'envoyer des e-mails au nom du domaine. Sans lui, les e-mails risquent de finir en spam et d'être plus faciles à imiter.

**Racine (apex) et `@`** — Le domaine lui-même, sans rien devant (`biblio-vss.fr`). Dans une zone DNS, on l'écrit `@`. `www.biblio-vss.fr` est un sous-domaine.

**TTL (Time To Live)** — La durée pendant laquelle un annuaire garde une réponse en mémoire avant de la redemander. C'est pour ça qu'un changement de DNS met de quelques minutes à quelques heures à se voir partout.

**Cache** — Une copie gardée sous la main pour répondre plus vite, sans refaire le même travail ou le même téléchargement. Pratique, mais elle peut être en retard sur la réalité (c'est pour ça qu'un changement de DNS met du temps à se voir partout). Le cache du navigateur permet aussi à une appli de s'ouvrir hors-ligne.

**Redirection 301** — La réponse « déplacé définitivement, va à cette adresse ». Le navigateur suit tout seul, et les moteurs de recherche mettent leurs liens à jour.

**Code 404** — La réponse « page introuvable ». Une page 404 personnalisée aide la personne perdue au lieu d'afficher une erreur brute.

**Origine** — Le trio protocole + domaine + port (`https://biblio-vss.fr`). Le navigateur range les données d'un site (localStorage, favoris) par origine : changer d'adresse, c'est repartir de zéro.

## Outils et collaboration (23 novembre)

**Plugin** — Une extension qu'on ajoute à un logiciel pour lui donner de nouvelles capacités sans modifier le logiciel lui-même. Impeccable est un plugin de Claude Code : il apporte des consignes de design et des commandes comme `/impeccable polish`.

**npm / npx** — *npm* est le grand catalogue public de programmes JavaScript (les « paquets ») et l'outil qui les installe. *npx* télécharge un paquet et l'exécute tout de suite : pratique, mais on lance du code qu'on n'a pas relu.

**Binaire** — Un programme déjà traduit en langage machine. Il s'exécute directement, mais on ne peut pas le relire comme du texte : il faut faire confiance à sa provenance.

**Empreinte (SHA-256)** — Une suite de caractères calculée à partir du contenu exact d'un fichier. Le moindre octet changé donne une empreinte totalement différente : la comparer à l'empreinte publiée prouve que le fichier n'a pas été modifié.

**Pull request (demande de fusion)** — Sur GitHub, la proposition d'intégrer les commits d'une branche dans une autre (souvent `main`). Elle montre les changements ligne par ligne, permet d'en discuter, puis on clique sur « Merge » pour fusionner.

**Fusion (merge)** — Réunir l'historique de deux branches. Si elles ont touché des fichiers différents, Git combine tout seul ; si elles ont modifié les mêmes lignes, il y a un conflit à trancher à la main.

**Polish (passe de finition)** — Une relecture d'interface qui corrige les détails (alignements, états des boutons, contrastes) sans changer l'identité ni le fonctionnement. Le contraire d'une refonte.

**Contraste** — L'écart de luminosité entre un texte et son fond, exprimé par un rapport (de 1 à 21). Les règles d'accessibilité demandent au moins 4,5 pour le texte courant, 3 pour les gros titres.

**Zone tactile** — La surface qu'on peut toucher du doigt pour activer un bouton. 44 px de côté au minimum, sinon on rate la cible ou on touche le bouton d'à côté.

**États d'un bouton** — Ses différentes apparences selon la situation : normal, survolé (souris dessus), appuyé, désactivé, avec le focus (sélectionné au clavier). Un bouton qui ne réagit pas paraît cassé.

**Revue UX (audit)** — Passer une interface en revue pour repérer ce qui gêne l'utilisateur. Une bonne revue mesure (tailles, contrastes, comportement sur petit écran) et classe les corrections par gravité, au lieu de donner des impressions.

**Zoom automatique (iPhone)** — Safari sur iPhone agrandit toute la page dès qu'on touche un champ dont le texte fait moins de 16 px. D'où la règle : texte des champs de saisie à 16 px minimum.

**Pseudo-élément (`::after`, `::before`)** — Un élément que le CSS ajoute à une balise sans toucher au HTML. Invisible, il sert ici à agrandir la zone tactile d'un bouton sans changer sa taille à l'écran.

**Marqueurs de conflit** — Quand Git ne peut pas fusionner seul, il écrit les deux versions dans le fichier entre `<<<<<<<` (ma version), `=======` et `>>>>>>>` (l'autre version). Résoudre le conflit, c'est remplacer ce bloc par la version voulue, puis enregistrer un commit de fusion.

## Passer à l'échelle (23 novembre)

**SaaS (Software as a Service)** — Un logiciel qu'on n'installe pas : on l'utilise en ligne, souvent avec un abonnement (Gmail, Notion). Derrière, l'éditeur doit faire tourner des serveurs pour des milliers de personnes à la fois, d'où les nombreux « étages » techniques.

**Vibe coding** — Programmer en décrivant ce qu'on veut à une IA, qui écrit le code. Ça produit vite quelque chose qui marche, mais faire un produit fiable demande encore de comprendre et de gérer tout ce qu'il y a autour.

**System design (conception du système)** — Le plan d'ensemble avant de coder : quelles grandes pièces (écran, serveur, base de données…), qui parle à qui, où vivent les données.

**Passer à l'échelle (scalabilité, scaling)** — La capacité d'un produit à tenir quand le nombre d'utilisateurs est multiplié par 10 ou par 1 000, sans ralentir ni tomber en panne.

**Site statique** — Un site fait uniquement de fichiers tout prêts (HTML, CSS, JS, JSON), sans programme qui calcule une réponse sur le serveur. Très rapide, peu cher, presque impossible à pirater côté serveur et capable d'encaisser beaucoup de visiteurs. C'est le cas de Biblio VSS.

**CI/CD (intégration et déploiement continus)** — Un robot (chez GitHub : *GitHub Actions*) qui, à chaque envoi de code, lance les tests (*intégration continue*) puis met en ligne si tout passe (*déploiement continu*). Il évite d'oublier une étape ou de publier une version cassée.

**GitHub Actions / workflow** — Le service de GitHub qui exécute ces robots. Un *workflow* est la recette, écrite dans `.github/workflows/`, qui dit quand se déclencher (à chaque push, chaque mois…) et quelles commandes lancer.

**GitHub Pages** — L'hébergement gratuit de sites statiques proposé par GitHub.

**CDN (Content Delivery Network)** — Un réseau de serveurs répartis dans le monde qui gardent une copie des fichiers du site : chaque visiteur est servi par le plus proche, donc plus vite, et la charge est partagée.

**Service worker** — Un petit script qu'un site installe dans le navigateur. Il intercepte les demandes de fichiers et peut répondre depuis le cache : c'est ce qui rend une PWA utilisable sans réseau.

**PWA (Progressive Web App)** — Un site qui se comporte comme une appli : il s'installe sur l'écran d'accueil et fonctionne hors-ligne, sans passer par un store.

**Rate limiting (limitation de débit)** — Plafonner le nombre de demandes qu'une même personne ou machine peut faire en un temps donné. Protège contre le spam, les attaques et les factures qui explosent (chaque appel à une IA est payant).

**Logs (journaux)** — Les lignes qu'un programme écrit au fil de son fonctionnement (« telle page demandée à 14 h 02 », « erreur ici »). On les relit pour comprendre ce qui s'est passé.

**Suivi des erreurs (error tracking)** — Un outil qui récupère automatiquement les plantages survenus chez les utilisateurs, avec le contexte, pour qu'on les corrige sans attendre qu'ils les signalent. Attention : il ne doit pas collecter de données personnelles.

**Monitoring et alertes** — Surveiller en continu qu'un service répond (et à quelle vitesse), et être prévenu·e (mail, notification) dès qu'il tombe.

**RLS (Row Level Security)** — Des règles écrites dans la base de données elle-même : elle vérifie, ligne par ligne, si la personne connectée a le droit de voir ou modifier cette donnée. Même si l'écran a un bug, la base refuse.

**RGPD** — Le règlement européen sur les données personnelles : ne collecter que le nécessaire, dire ce qu'on en fait, permettre de les supprimer, protéger davantage les mineurs et les données sensibles.

**Privacy by design (protection dès la conception)** — Choisir dès le départ une architecture qui collecte le moins possible (pas de compte, pas de pistage, données sur l'appareil) plutôt que protéger après coup des données qu'on n'aurait pas dû garder.

## Retours sur une maquette (24 novembre, après-midi)

**ISBN** — Le numéro unique d'un livre (13 chiffres, celui du code-barres). Chaque édition a le sien : le poche et le grand format n'ont pas le même.

**Aplat** — Une surface de couleur unie, sans variation. À ne pas confondre avec un **dégradé**, où une couleur passe progressivement à une autre.

**Fenêtre modale (`<dialog>`)** — Une fenêtre qui s'ouvre par-dessus la page : tant qu'elle est ouverte, le reste passe sous un voile et ne réagit plus.

**`:has()`** — Un sélecteur CSS récent qui veut dire « si l'élément contient… ». Exemple : « si la page contient une fenêtre ouverte, cache tel bouton ».

**`color-scheme`** — Une propriété CSS qui dit au navigateur si la page est claire ou sombre, pour qu'il dessine les cases, listes et barres de défilement dans les bonnes couleurs.

**`appearance: none`** — Une instruction CSS qui retire le dessin d'un élément de formulaire par le système (une case à cocher, par exemple), pour le dessiner soi-même.

**`aria-expanded`** — Un attribut qui dit au lecteur d'écran si un bouton « Afficher plus » est ouvert ou fermé.

**Flexbox** — Une façon de ranger des éléments en ligne ou en colonne en CSS. La règle `flex: 1` dit « prends toute la place qui reste ».

**Service worker (cache hors-ligne)** — Un petit programme qui garde une copie de l'appli sur le téléphone pour qu'elle marche sans connexion. Il ne recharge les fichiers que si son numéro de version change.

**Droit de courte citation** — L'exception au droit d'auteur qui permet de citer un court extrait dans une analyse, avec sa source. Recopier tout un résumé officiel va au-delà : c'est toléré en pratique, pas garanti.

