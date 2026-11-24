# Taste Skill : fiche mémoire

Une *skill* (dossier de consignes et de scripts pour un agent de code) qui sert à construire des **sites vitrines** :
https://github.com/leonxlnx/taste-skill (licence MIT). Essayée le 10 novembre 2026, version 2.5.1, sur un café inventé (« Velgane », Nantes).

## Quand l'utiliser
- **Oui** : une page vitrine pour un commerce, un indépendant, un produit, un logiciel.
- **Non** : *Budget du foyer* ou toute appli qu'on utilise au quotidien. Ses règles (une section par écran, grande photo d'accueil) ne conviennent pas à un outil.

## Ce que l'essai a montré
- Le contrôle final (`gate.mjs`) est utile : 11 défauts au premier tour, 1 au deuxième, 0 au troisième.
- **Les contrôles de texte sont pensés pour l'anglais.** Une page en français passe, mais plusieurs vérifications de rédaction (verbes des boutons, noms attendus dans les titres) ne reconnaissent pas les mots français : relire le texte soi-même.
- **Sans photos du client, la page reste un brouillon** : toutes les photos sont des images libres d'un autre lieu, à remplacer. La bibliothèque est riche pour un café (une douzaine), pauvre pour une boulangerie (4) ou un fleuriste (3).
- Les prix, les horaires et le nom étaient inventés pour l'essai ; la skill oblige à les marquer (`data-assumed`) et à les lister.

## Marche à suivre dans une session cloud (pour Claude)
1. Environnement « Sites vitrines (photos Wikimedia) » : il autorise `upload.wikimedia.org` et `commons.wikimedia.org`, d'où viennent les photos. Dans l'environnement par défaut, ces sites sont bloqués.
2. Cloner le dépôt dans un dossier à part, lire `skills/taste-skill/SKILL.md` et suivre sa section « The run ». Construire le site dans un autre dossier.
3. Lancer chaque script Node avec `NODE_USE_ENV_PROXY=1` : sans cela, Node ignore le proxy de la session et les téléchargements restent bloqués.
4. Chrome refuse de démarrer tel quel (la session tourne en « root »). Créer ce lanceur et le donner dans `CHROME_PATH` :
   ```sh
   #!/bin/sh
   exec /opt/pw-browsers/chromium --no-sandbox ${HTTPS_PROXY:+--proxy-server="$HTTPS_PROXY"} --proxy-bypass-list="127.0.0.1;localhost" "$@"
   ```
5. Après `photos.mjs fetch`, réencoder les images : certaines sortent avec un en-tête faux que Chrome refuse d'afficher (contrôle `empty-visual`).
   ```sh
   for f in assets/img/*.webp; do ffmpeg -v error -y -i "$f" -c:v libwebp -q:v 84 "$f.tmp.webp" && mv "$f.tmp.webp" "$f"; done
   ```
6. Le contrôle final n'accorde que trois tours : corriger tous les défauts d'un tour avant de relancer.
7. La skill déclare un *hook* « Stop » (script lancé à la fin de chaque réponse). Lu le 10/11 : il ne fait que lancer `gate.mjs` en local. Relire `SKILL.md` et `scripts/gate.mjs` si la version a changé.

## Ce qui n'est pas conservé
La page d'essai elle-même n'est dans aucun dépôt (le carnet ne garde pas le code). Pour un vrai site, créer un dépôt dédié.
