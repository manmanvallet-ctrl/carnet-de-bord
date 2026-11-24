# Les étages d'un vrai produit

Point de départ : une vidéo qui oppose « vibe coding = un prompt, un site » à la pile de 16 étages d'un vrai **SaaS** (un logiciel en ligne utilisé par beaucoup de monde). Mon ambition : que mes projets soient utilisés par beaucoup plus de personnes que moi. Ce fichier dit, pour chaque projet, quels étages sont déjà construits, lesquels manquent, et **à quel moment** il faudra les monter.

> Règle : on monte un étage quand le projet en a besoin, pas avant. Mais on sait qu'il existe et on prévoit sa place.

Légende : ✅ fait · 🟡 en partie / prévu · ⬜ pas encore · ➖ inutile pour ce projet (et c'est voulu)

*État au 23 novembre 2026.*

## Le tableau

| Étage | Budget du foyer | Club Ciné | Biblio VSS |
|---|---|---|---|
| **System design** (le plan d'ensemble) | ✅ `PLAN.md`, `VISION.md` | ✅ `docs/discovery.md` | 🟡 dans le README |
| **Architecture** (les pièces et leurs liens) | ✅ modules JS, calculs séparés de l'affichage | ✅ React + TypeScript, données à part | ✅ site statique + appli Android/iOS (Capacitor) |
| **Frontend** | ✅ | ✅ prototype | ✅ |
| **APIs & backend** | ⬜ tout tourne sur le téléphone | 🟡 Supabase prévu, pas encore branché | ➖ pas de serveur : c'est un choix de sécurité |
| **Base de données** | 🟡 stockage local / artefact, migrations ✅ | 🟡 schéma Supabase prêt | ✅ fichiers JSON dans le dépôt |
| **Auth & permissions** | ⬜ | 🟡 règles RLS écrites et testées | ➖ aucun compte, rien à protéger côté utilisateur |
| **Hébergement** | 🟡 artefact claude.ai | 🟡 artefact de démo | ✅ GitHub Pages + stores à venir |
| **CI/CD & versions** | 🟡 Git ✅, tests lancés à la main | 🟡 Git ✅ | ✅ mise en ligne et appli Android construites automatiquement |
| **Sécurité** | 🟡 dépôt privé, données réelles | 🟡 RLS | ✅ sortie rapide, pas de pistage, page confidentialité |
| **Rate limiting** | ⬜ | ⬜ | ⬜ formulaire « Proposer » sans protection anti-spam visible |
| **Cache & CDN** | ➖ | ➖ | ✅ hors-ligne (service worker) + CDN de GitHub Pages |
| **Suivi des erreurs & logs** | ⬜ | ⬜ | ⬜ |
| **Monitoring & alertes** | ⬜ | ⬜ | ⬜ |
| **Tests** | ✅ unitaires + parcours | 🟡 tests de la base (RLS), rien sur l'écran | ⬜ aucun test automatique |
| **Scaling** (tenir la charge) | ➖ pour l'instant | ⬜ dépendra de Supabase | ✅ un site statique encaisse la foule tout seul |

## Ce que ce tableau m'apprend

- **Biblio VSS est le projet le plus prêt à être utilisé par beaucoup de monde.** Le choix « pas de serveur, pas de compte » règle d'avance la sécurité des comptes, le scaling et une bonne partie de la vie privée. Ce qui lui manque : **des tests automatiques** et une **protection du formulaire** contre le spam.
- **Club Ciné a la base solide** (règles d'accès testées), mais tout reste à brancher. Le seuil à ne pas franchir sans préparation : de **vrais élèves mineurs**, donc RGPD, comptes enseignant·es et relecture du contenu rédigé par IA.
- **Budget du foyer est le plus loin d'un usage large.** Il manipule des **données bancaires** : pour l'ouvrir à d'autres foyers, il faudra un backend, des comptes, un stockage chiffré, le RGPD, et protéger la **clé d'API du coach IA** (côté serveur, avec une limite d'appels : sinon un seul utilisateur peut faire exploser la facture).

## Les portes à franchir avant d'ouvrir au public

| Projet | À faire avant d'ouvrir |
|---|---|
| Biblio VSS | Tests automatiques lancés par GitHub à chaque envoi · anti-spam sur « Proposer » · savoir quand le site tombe (monitoring simple) · un suivi des erreurs **qui ne piste personne** |
| Club Ciné | Brancher Supabase et les comptes · RGPD pour des mineurs (accord de l'établissement, données minimales) · contenu relu par l'enseignant·e · hébergement réel · tests des écrans |
| Budget du foyer | Décider si c'est un produit pour d'autres foyers · backend + comptes + chiffrement · clé IA côté serveur + limite d'appels · RGPD · faire lancer les tests par GitHub (CI) |

## Mon avis (Claude)

L'ordre le plus rentable : **Biblio VSS d'abord** (le plus proche du public, peu d'étages manquants), puis Club Ciné, puis Budget. L'étage qui manque partout et qui coûte le moins : **les tests lancés automatiquement par GitHub**. C'est lui qui permet de continuer à modifier un projet utilisé par des inconnus sans le casser.
