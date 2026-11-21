# Mon application Flask

## Liens
- Image Docker Hub : https://hub.docker.com/r/chahedbenabdallah/app
- Versions (tags) : https://hub.docker.com/r/chahedbenabdallah/app/tags
- Code source (GitHub) : https://github.com/Chahedbenabdallah/mini-projet-docker

Petite application web qui affiche un message d'accueil configurable.

## Image Docker Hub
`chahedbenabdallah/app` : versions `1.0.0`, `1.0.1`, alias `1.0`

## Lancer
```bash
docker run -d --name mon-app -p 8080:5000 \
  -e MESSAGE="Bonjour" --memory 256m --cpus 0.5 \
  chahedbenabdallah/app:1.0.1
```
Puis ouvrir http://localhost:8080

## Construire (optionnel)
```bash
docker build -t chahedbenabdallah/app:1.0.1 .
```

## Variables d'environnement
| Variable | Défaut | Rôle |
|---|---|---|
| MESSAGE | Bonsoir depuis Docker ! | Message affiché sur la page d'accueil |

## Arrêter
```bash
docker rm -f mon-app
```
