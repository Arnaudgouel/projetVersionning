# Projet Versionning

## Clone the project via SSH

```bash
git clone git@github.com:Arnaudgouel/projetVersionning.git
```

## Create Branch into repository

```bash
git checkout -b <branchName>
```

## Check current files status

```bash
git status
```

## Stage changes

```bash
git add <fileName>
```

## Commit changes

```bash
git commit -m "<commitDescription>"
```

### Commit's name conventions

[Go to official site](https://www.conventionalcommits.org/en/v1.0.0/)

- `build`: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- `chore`: Miscellaneous commits e.g. modifying `.gitignore`
- `ci`: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- `docs`: Documentation only changes
- `feat`: A new feature (**MINOR** version)
- `fix`: A bug fix (**PATCH** version)
- `perf`: A code change that improves performance
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- `test`: Adding missing tests or correcting existing tests
- `ops` Commits, that affect operational components like infrastructure, deployment, backup, recovery, ...

## Workflow

1. Faire un git status pour voir si on a pas des changements non validés
1. Se placer sur la branche principale (staging) et se mettre à jour

```bash
git pull origin staging
```

1. Création d'une nouvelle branche (**Respecter la convention de nommage comme pour les commit, le nom de branche doit être la synthèse des commits de cette branche**) pour effectuer un développement

```bash
git checkout -b <branchName>
```

1. Faire un git status pour voir les fichiers changés
1. Indexer les fichiers voulus
1. Effectuer un commit avec message en respectant la convention de nommage
1. Envoyer le(s) commit(s) sur le repo distant
1. Créer une pull request sur github ![pr github](docs/img/pr-github.png)
1. Mettre en reviewer une autre personne pour qu'elle valide les changements
