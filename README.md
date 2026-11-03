# Compagnie Guides VDA — site de la compagnie

Site de la compagnie guides du groupe Ville-d'Avray – Sèvres (Bienheureux Frédéric Ozanam, Scouts Unitaires de France).

## Contenu

- `site/index.html` : le site (une seule page HTML, sans dépendance à installer).
- `site/img/` : les photos de la page d'accueil.
- `data/lieux.json` : la liste des lieux de camp (liste CE – WE & camp de Pâques), qui alimente l'onglet « Lieux de camp ».

## Onglets

- **Accueil** et **Programme** (publics) : programme 2026-2027 et prochain rendez-vous (lieu, horaires) pour les parents.
- **Fiche de préparation** : formulaire vide que les équipes remplissent avant chaque sortie ; les réponses n'arrivent que dans l'espace cheftaines.
- **Espace cheftaines** (code d'accès) : programme, tâches, lieux de camp, budget & repas, fiches reçues par équipe, composition des équipes.
- **Serval, Renard, Faucon, Panthères, Ocelot** : tâches de l'équipe, suivi des lieux (non contacté / contacté / accepté / refus), budget & repas, horaires et lieu de rendez-vous de l'équipe.

## Où vivent les données

Le site publié tourne comme artifact Claude (claude.ai). Les données partagées (programme, tâches, statuts des lieux, budgets, repas, fiches) sont stockées dans la base de l'artifact, pas dans ce dépôt. Ouvert en dehors de claude.ai (par exemple via GitHub Pages), la page s'affiche mais sans données ni enregistrement.
