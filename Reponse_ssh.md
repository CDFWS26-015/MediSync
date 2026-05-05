
## Contrainte réseau — Port SSH 22 bloqué
Le port SSH 22 est bloqué sur le réseau de l'établissement. La commande suivante échoue :
```
git push git@github.com:user/repo.git# ssh: connect to host github.com port 22: Connection timed out
```

Solution retenue — Partage de connexion mobile
La solution la plus directe et la plus rapide a été de contourner la restriction réseau en changeant de réseau.
Nous avons utilisé un partage de connexion mobile (hotspot smartphone), qui ne présente pas les restrictions du réseau de l'établissement. Le port SSH 22 étant accessible depuis ce réseau, aucune configuration supplémentaire n'a été nécessaire.

```
# Aucune modification de configuration requise# Connexion SSH standard une fois sur le réseau mobilessh -T git@github.com# Hi username! You've successfully authenticated...

git push origin main
```

Remarque : Des solutions alternatives existent si le changement de réseau n'est pas possible, comme l'utilisation de SSH sur le port 443 ou le protocole HTTPS avec Personal Access Token, mais elles n'ont pas été nécessaires dans notre cas.

