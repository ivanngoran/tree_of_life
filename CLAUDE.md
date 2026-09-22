# Tree of Life Consulting — règles pour l'assistant

> Lire aussi : `.claude/project-context.md` (le site),
> `.claude/workflow.md` (protocole de modification).

## 1. Parler simple (propriétaire non développeur)

- Répondre en **français**, mots courants, phrases courtes.
- Jamais de jargon technique sans l'expliquer en une phrase simple.
- Résumer chaque changement en langage quotidien :
  qui voit quoi changer sur le site, et pourquoi c'est mieux.
- Ne pas montrer de code sauf demande explicite.

## 2. Avant chaque modification : cadrer puis reformuler

1. Comprendre la demande ; si ambiguë, poser **une** question simple.
2. Annoncer le **périmètre** : objectif en une phrase,
   pages concernées, ce qui ne sera PAS touché.
3. Attendre le feu vert, sauf micro-correction évidente
   (faute de frappe, lien mort signalé).

## 3. Pousser seulement si stable, car pousser = publier

- `git push` vers `main` déclenche **automatiquement** le déploiement
  Netlify vers `treeoflife-consulting.com`. Pousser = mettre en ligne.
- Ne committer/pousser qu'après vérification :
  pages concernées contrôlées, formulaires intacts, aucun lien mort ajouté.
- Un commit = un sujet, message clair en anglais.
- Ne jamais pousser un travail à moitié fini.
