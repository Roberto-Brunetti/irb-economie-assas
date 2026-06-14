# Site web — IRB en économie · Université Paris Panthéon-Assas

Site statique du comité d'évaluation éthique de la recherche (Institutional Review Board en
économie), prêt à être publié sur **GitHub Pages**.

## Contenu

| Fichier | Rôle |
|---|---|
| `index.html` | Page unique du site (présentation, composition, saisine, avis, documents, références, contact) |
| `assets/style.css` | Feuille de style |
| `documents/` | Documents téléchargeables (règlement, formulaire de saisine) |
| `.nojekyll` | Empêche GitHub de retraiter le site avec Jekyll |

## Publier sur GitHub Pages

1. Créer un dépôt GitHub (par ex. `irb-assas`) et y pousser le **contenu de ce dossier**
   (`index.html` doit être à la racine du dépôt) :
   ```bash
   cd Site_IRB-Assas
   git init
   git add .
   git commit -m "Site IRB en économie — version initiale"
   git branch -M main
   git remote add origin https://github.com/<utilisateur>/irb-assas.git
   git push -u origin main
   ```
2. Sur GitHub : **Settings → Pages → Build and deployment → Source : Deploy from a branch**,
   branche `main`, dossier `/ (root)`, puis **Save**.
3. Le site est publié sous quelques minutes à l'adresse
   `https://<utilisateur>.github.io/irb-assas/`.

> Pour une adresse personnalisée (`integrite.u-paris2.fr`, etc.), ajouter un fichier `CNAME`
> et configurer le DNS auprès du service informatique de l'Université.

## À finaliser avant la mise en ligne publique

- **Adresse e-mail de contact** — remplacer le `mailto:` provisoire dans `index.html`
  (section *Contact*, marqué « adresse à confirmer ») par l'adresse publique réelle de l'IRB.
- **Présidence / vice-présidence** — une fois élues, indiquer les noms dans la section
  *Composition*.
- **Prénoms complets des membres internes** — actuellement affichés avec l'initiale, comme dans
  le document source ; à compléter si souhaité.
- **Documents** — les `.docx` du dossier `documents/` contiennent encore des champs à finaliser
  (adresse e-mail et URL du site). Penser à les régénérer (idéalement en PDF) avant publication,
  et à ajouter le modèle de notice d'information et le modèle de consentement éclairé.
- **URL du site** — reporter l'adresse GitHub Pages finale dans le règlement (mention « (LIEN) »).

## Aperçu local

Ouvrir simplement `index.html` dans un navigateur, ou lancer un petit serveur :
```bash
cd Site_IRB-Assas
python -m http.server 8000   # puis http://localhost:8000
```
