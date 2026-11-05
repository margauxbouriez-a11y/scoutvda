# Compagnie Guides VDA — site de la compagnie

Site de la compagnie guides du groupe Ville-d'Avray – Sèvres (Bienheureux Frédéric Ozanam, Scouts Unitaires de France).

## Contenu

- `index.html` : le site (une seule page HTML, sans dépendance à installer), servi par GitHub Pages.
- `img/` : les photos de la page d'accueil.
- `data/programme.json` : le programme 2026-2027 affiché par la version GitHub Pages.
- `data/lieux.json` : la liste des lieux de camp (liste CE – WE & camp de Pâques).

## Onglets

- **Accueil** et **Programme** (publics) : programme 2026-2027 et prochain rendez-vous (lieu, horaires) pour les parents.
- **Fiche de préparation** : formulaire vide que les équipes remplissent avant chaque sortie ; les réponses n'arrivent que dans l'espace cheftaines.
- **Espace cheftaines** (code d'accès) : programme, tâches, lieux de camp, budget & repas, fiches reçues par équipe, composition des équipes.
- **Serval, Renard, Faucon, Panthères, Ocelot** : tâches de l'équipe, suivi des lieux (non contacté / contacté / accepté / refus), budget & repas, horaires et lieu de rendez-vous de l'équipe.

## Où vivent les données

Le site publié tourne comme artifact Claude (claude.ai). Les données partagées (programme, tâches, statuts des lieux, budgets, repas, fiches) sont stockées dans la base de l'artifact, pas dans ce dépôt. Sur GitHub Pages, le site est en lecture seule : l'accueil et le programme s'affichent à partir de `data/programme.json`, mais rien ne peut être enregistré (fiches, tâches, lieux, budgets). Quand le programme change sur claude.ai, il faut mettre à jour `data/programme.json`.
