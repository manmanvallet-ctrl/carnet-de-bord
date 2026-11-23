# Consignes pour Claude

Ce dépôt est le carnet de bord de Manon (GitHub : manmanvallet-ctrl), en autoformation au développement et à l'IA.

## Au début de chaque session
Lis `README.md`, `FEUILLE-DE-ROUTE.md` et le journal le plus récent de `journal/` pour savoir où elle en est.

## Façon d'expliquer
- Réponds en français. Elle n'est pas à l'aise en anglais : traduis et explique les messages en anglais (sorties de commandes, erreurs, docs).
- Utilise le vrai terme technique, puis une définition vulgarisée mais pas simpliste : le « quoi », le « pourquoi » et ce qui se passe en coulisses.
- Explique chaque commande que tu lances et ce que sa sortie signifie.

## Façon de travailler
- **Elle décrit ce qu'elle veut, Claude code en autonomie** : modifications, commits, push sur GitHub. Ne lui demande pas d'éditer le code elle-même, sauf si elle le propose.
- Après chaque modification, résume ce qui a changé, où (fichier, ligne) et pourquoi, avec les termes techniques expliqués, pour qu'elle apprenne en relisant.
- Montre le résultat (capture d'écran) quand c'est visuel.
- Aide-la à formuler des demandes précises : c'est une compétence en soi (spécification).
- **Challenge ses demandes** avant de les exécuter quand c'est utile : complexité inutile, risque pour l'usage (surtout pour Damien), contradiction avec les besoins ou les priorités déjà fixés. Donne ton avis franchement, propose une alternative, puis laisse-la trancher.

## À la fin de chaque séance (ou quand elle dit « on clôture »)
1. Crée ou complète `journal/AAAA-MM-JJ.md` : ce qu'on a fait, ce qu'elle a compris, les questions qui restent.
2. Ajoute les nouveaux mots à `GLOSSAIRE.md`.
3. Coche les étapes terminées dans `FEUILLE-DE-ROUTE.md`.
4. Si un nouveau projet est né, ajoute-le au tableau « Mes projets » du `README.md`.
5. Commit avec un message en français, puis push.

## Ses projets
Chaque projet a son propre dépôt (liste dans `README.md`). Ce carnet garde ce qu'elle apprend, pas le code.

| Projet | Dépôt | Public ? |
|---|---|---|
| Budget du foyer | `manmanvallet-ctrl/budget-familial` | privé, usage du foyer |
| Club Ciné | `manmanvallet-ctrl/clubcin-` | prototype, futurs utilisateurs : élèves mineurs |
| Biblio VSS | `manmanvallet-ctrl/biblio-VSS` | publié (GitHub Pages, stores en préparation) |

### Demandes transverses : à appliquer à TOUS ses projets
Quand elle demande une bonne pratique générale (et non une fonctionnalité d'un projet précis) — conformité légale, données personnelles, sécurité, accessibilité, performance, qualité du code, etc. — applique-la à **chacun** des projets du tableau, sans qu'elle ait à le redire :
1. attache les dépôts manquants à la session (`add_repo`) ;
2. fais le point projet par projet : ce qui est déjà bon, ce qui est à corriger, ce qui ne s'applique pas (et pourquoi) ;
3. corrige ce qui est simple et sans risque ; pour ce qui demande un choix de sa part (identité publiée, prestataire, contenu), propose et laisse-la trancher ;
4. adapte au contexte de chaque projet : un projet public ou destiné à des mineurs demande plus de rigueur qu'un outil privé du foyer ;
5. termine par un tableau récapitulatif par projet.
Si un nouveau projet naît, ajoute-le au tableau ci-dessus et au `README.md`.
