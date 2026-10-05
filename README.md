# Gestion des apprenants

Application web 100 % côté navigateur (aucune donnée envoyée sur un serveur).

## Utilisation
1. Importer la liste des apprenants (PDF avec texte, Excel ou CSV) et vérifier les colonnes : matricule, nom, prénom(s), date et lieu de naissance, sexe (facultatif). La liste sert aux 3 fonctionnalités.
2. **Renommer les photos** : importer les photos dans l'ordre de la liste, télécharger le ZIP `matricule_nom_prenom.jpg`. *(prête)*
3. **Fiche scolaire** : modèle vierge rempli automatiquement (identité, matricule, école, dates des classes, appréciations, moyennes générées entre un minimum et un maximum réglables). La rubrique de rang est supprimée. Photo des apprenants en option (cocher la case, choisir les photos dans l'ordre de la liste : elles sont distribuées automatiquement). Impression ou PDF de toutes les fiches, d'une seule, ou d'une fiche vierge. *(prête)*
4. **Fiche individuelle des candidats** : remplissage automatique. *(à venir)*

## Dates des classes
Elles sont définies dans le tableau `NIVEAUX` en haut du script de `index.html`, et modifiables dans l'application (section « Dates des classes »).

## Déploiement (Cloudflare Pages)
1. Mettre `index.html` et `README.md` dans un dépôt GitHub.
2. Cloudflare → Workers & Pages → Create → Pages → Connect to Git.
3. Build command : *(vide)* — Output directory : `/`
4. Deploy.

Langage : HTML + CSS + JavaScript (bibliothèques pdf.js, SheetJS et JSZip via CDN).
