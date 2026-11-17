# Morocco 2030 — Semantic Tourism

Plateforme Web sémantique pour explorer le tourisme marocain à partir d’un Knowledge Graph RDF, dans le contexte de la Coupe du monde 2030.

Le cahier des charges complet fourni pour le projet est conservé dans [`docs/Projet_Semantic_Web_V1.pdf`](docs/Projet_Semantic_Web_V1.pdf). Son résumé opérationnel est dans [`docs/brief.md`](docs/brief.md).

## Objectif

Intégrer des données touristiques marocaines issues de sources hétérogènes dans un graphe RDF, puis les exploiter avec SPARQL dans une application Web qui permet la recherche, la consultation de fiches et la navigation entre ressources liées.

## Exigences de départ

- Intégrer au moins trois sources ou jeux de données distincts et au moins deux formats ou modes d’accès.
- Définir une ontologie RDF/RDFS, avec OWL lorsque cela apporte une inférence utile, et des URI stables.
- Conserver la provenance, les licences et les dates de collecte disponibles.
- Alimenter les fonctions de recherche et de navigation avec des requêtes SPARQL.
- Publier des métadonnées structurées, par exemple en JSON-LD.
- Vérifier les informations sur les stades, matchs, horaires, distances et affectations. Toute donnée non confirmée officiellement doit être signalée comme illustrative ou candidate.

## Architecture et outils proposés

Le sujet recommande Java, Apache Jena, Fuseki, Spring Boot, HTML/Bootstrap/JavaScript et JSON-LD. Cette stack est une proposition de départ à confirmer par l’équipe. L’architecture cible sépare l’intégration des données, l’ontologie, le triple store, le backend, le frontend et la publication des métadonnées.

## Organisation

```text
docs/       Cahier des charges et notes du projet
data/       Règles de collecte, provenance et organisation des données
ontology/   Conception de l’ontologie et des URI
queries/    Requêtes SPARQL et scénarios associés
```

Le dépôt contient pour l’instant le cadrage et la structure documentaire. Les sources de données, l’ontologie, les requêtes et les composants de l’application seront ajoutés au fur et à mesure des décisions de l’équipe.

## Démarrage

Lire [`docs/brief.md`](docs/brief.md), puis décider du périmètre touristique, des utilisateurs cibles et des premières questions auxquelles l’application répondra. Aucune application exécutable n’est encore configurée.
