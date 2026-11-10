# Compagnie Guides VDA — site de la compagnie

Site de la compagnie guides du groupe Ville-d'Avray – Sèvres (Bienheureux Frédéric Ozanam, Scouts Unitaires de France).

## Contenu

- `index.html` : le site (une seule page HTML, sans dépendance à installer), servi par GitHub Pages.
- `img/` : les photos de la page d'accueil.
- `data/programme.json` : le programme 2026-2027 affiché par la version GitHub Pages.
- `data/lieux.json` : la liste des lieux de camp (liste CE – WE & camp de Pâques).

## Onglets

- **Accueil** et **Programme** (publics) : programme 2026-2027 et prochain rendez-vous (lieu, horaires) pour les parents.
- **Présences** : chaque guide indique oui ou non pour chaque rendez-vous, équipe par équipe.
- **Fiche de préparation** : formulaire vide que les équipes remplissent avant chaque sortie ; les réponses n'arrivent que dans l'espace cheftaines.
- **Espace cheftaines** (code d'accès) : programme, tâches, lieux de camp, budget & repas, fiches reçues par équipe, composition des équipes.
- **Serval, Renard, Faucon, Panthères, Ocelot** : tâches de l'équipe, suivi des lieux (non contacté / contacté / accepté / refus), budget & repas, horaires et lieu de rendez-vous de l'équipe.

## Où vivent les données

Le site publié sur GitHub Pages lit et enregistre ses données (programme, présences, fiches, tâches, statuts des lieux, budgets, repas) dans n8n :

- data table **compagnie_vda_site** (colonnes `col`, `docid`, `data` en JSON) ;
- workflow **Site compagnie VDA – données**, avec deux webhooks :
  - `GET  https://margauxbouriez2.app.n8n.cloud/webhook/compagnie-vda/data` renvoie tous les documents ;
  - `POST https://margauxbouriez2.app.n8n.cloud/webhook/compagnie-vda/write` avec `{op: "set" | "update" | "delete", c, id, d}`.

Le site recharge les données à l'ouverture, au retour sur l'onglet et toutes les 45 secondes. Chaque lecture ou écriture compte comme une exécution n8n.

`data/programme.json` sert de secours : si n8n ne répond pas, la page affiche le programme en lecture seule.
