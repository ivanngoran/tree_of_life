# Contexte projet — Tree of Life Consulting

Site vitrine statique, sans outil de construction : des pages HTML simples,
un fichier de styles partagé, un fichier de scripts partagé.

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | Accueil (présentation, services, fondatrice, avis, guide gratuit) |
| `about.html` | Histoire de la fondatrice, diplômes |
| `coaching.html` | Formules de coaching individuel |
| `programs.html` | Programmes de groupe |
| `consulting.html` | Conseil RH / entreprise + étude de cas |
| `contact.html` | Formulaire de contact |
| `booking.html` | Réservation d'appel gratuit (date, heure, fuseau horaire) |
| `privacy.html` | Politique de confidentialité |
| `assets/` | Logos et icônes (images partagées) |
| `styles.css` / `main.js` | Styles et comportements communs à toutes les pages |
| `netlify.toml` | Réglages d'hébergement Netlify |
| `robots.txt` / `sitemap.xml` | Référencement (domaine `treeoflife-consulting.com`) |

## Formulaires (données via Netlify, sans serveur)

Trois formulaires, repérables à `data-netlify="true"` — **ne jamais retirer
cet attribut ni les champs cachés `form-name` / `bot-field`** :

- `contact` (contact.html) : message simple, confirmation `?ok=1`
- `guide` (index.html) : email pour recevoir le guide gratuit, `?guide=ok`
- `booking` (booking.html) : créneau + fuseau horaire détecté automatiquement,
  heure convertie en temps universel (champ caché `utc_datetime`), `?booked=1`

Règle d'or : le visiteur choisit dans **son** fuseau, le site enregistre en
temps universel. Ne pas toucher au script de conversion sans test.

## Publication

Pousser vers la branche `main` sur GitHub met le site en ligne
automatiquement (Netlify déploie tout seul). Voir `workflow.md`.
