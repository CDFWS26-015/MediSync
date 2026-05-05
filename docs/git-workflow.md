# Questions de Méthodologie et Technique Git

## Mise en œuvre technique

**T1 — Quel est le protocole de communication utilisé en standard par le client git ?**
Le protocole utilisé en standard est le protocole **SSH** (Secure Shell). Il permet une communication sécurisée et authentifiée via une paire de clés (publique et privée).

**T2 — Quel est le protocole de communication utilisé en secours par le client git ?**
Le protocole de secours est le protocole **HTTPS**. Il est couramment utilisé lorsque les restrictions réseau (pare-feu) bloquent les ports dédiés au SSH.

**T3 — Est-il possible de synchroniser avec plusieurs dépôts distants un dépôt local ? Si oui, comment ?**
Oui, c'est possible. Un dépôt Git peut avoir plusieurs "remotes". On peut en ajouter de nouveaux avec la commande `git remote add <nom> <url>`. Par exemple, on peut pousser son code vers GitHub et GitLab simultanément.

**T4 — Un fichier a été ajouté au dépôt par mégarde via un commit. Ce commit a été annulé via la commande git revert. Quel est l’effet de cette commande sur le dépôt Git ?**
La commande `git revert` crée un **nouveau commit** qui contient l'inverse des modifications apportées par le commit ciblé. Contrairement à un reset, l'historique n'est pas effacé : le commit d'erreur reste visible, et le commit de correction s'ajoute par-dessus.

---

## Mise en œuvre méthodologique

**M1 — Quelle différence principale constatez-vous entre git merge et git rebase en termes de gestion de l'historique ?**
`git merge` conserve l'historique réel en créant un "commit de fusion" qui relie les branches (historique non-linéaire). `git rebase` réécrit l'historique en déplaçant les commits de la branche de fonctionnalité au sommet de la branche principale, créant ainsi un historique **linéaire** et plus lisible.

**M2 — Quelle autre méthode de branching que GitHub Flow avez-vous abordée ? En quoi diffère-t-elle ?**
La méthode **GitFlow**. Elle diffère de GitHub Flow par sa complexité : là où GitHub Flow n'utilise qu'une seule branche principale, GitFlow utilise deux branches à longue durée de vie (`main` pour la production et `develop` pour l'intégration) ainsi que des branches spécifiques pour les versions (`release`) et les correctifs (`hotfix`).

**M3 — Quel est l'objectif concret d'une pull request / merge request dans le travail en équipe ?**
L'objectif principal est la **revue de code** (Code Review). Cela permet aux autres membres de l'équipe de vérifier la qualité, la logique et l'absence de bugs dans le code proposé avant qu'il ne soit officiellement intégré à la branche principale.