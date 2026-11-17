# Résumé du cahier des charges

## Sujet

**Morocco 2030 — Semantic Tourism** : concevoir une plateforme Web sémantique pour valoriser le tourisme marocain. Le contexte de la Coupe du monde 2030 sert de point d’entrée pour découvrir les destinations, le patrimoine, la culture et les expériences du pays.

## Résultat attendu

Une application fonctionnelle qui intègre des données hétérogènes dans un Knowledge Graph RDF. Elle identifie les ressources avec des URI stables, les décrit avec une ontologie et des vocabulaires réutilisés, les stocke dans un triple store, les interroge en SPARQL et expose des métadonnées structurées.

## Fonctionnalités obligatoires

- Rechercher des villes, sites touristiques, monuments, activités ou d’autres ressources du périmètre choisi.
- Afficher une fiche avec nom, description, catégorie, localisation, source et relations connues.
- Naviguer entre les ressources à partir des relations du graphe.
- Alimenter les fonctions par des requêtes SPARQL.
- Utiliser au moins trois sources ou jeux de données réellement distincts, couvrant au moins deux formats ou modes d’accès.
- Exposer des métadonnées RDF/JSON-LD ou un mécanisme équivalent, avec des identifiants stables.
- Documenter la provenance, les sources, les licences et les dates de collecte disponibles.

Carte, filtres, recherche de proximité, circuits touristiques, visualisation du graphe et démonstration d’inférence RDFS/OWL sont recommandés si le périmètre et les données le permettent.

## Intégrité et qualité des données

Les pistes de sources du sujet incluent OpenStreetMap, Wikidata, Visit Morocco, FIFA et les portails Open Data marocains. L’équipe doit vérifier l’accès, la couverture, la qualité, les licences, les obligations d’attribution et les limites de chaque source avant utilisation.

Ne pas présenter comme faits définitifs des informations non confirmées sur les villes, stades, matchs, horaires, distances ou affectations liés à la compétition. Les données non officielles doivent être explicitement marquées comme illustratives ou candidates.

## Architecture et stack suggérées

Le flux conseillé est : collecte → nettoyage et transformation RDF → attribution d’URI et rapprochement → chargement dans le triple store → API et requêtes SPARQL → interface Web → publication de métadonnées.

Le sujet recommande Java et Apache Jena pour le pipeline RDF, Apache Jena Fuseki comme triple store, Spring Boot pour l’API, et HTML/Bootstrap/JavaScript pour l’interface. JSON-LD est proposé pour les métadonnées. L’équipe peut choisir une autre stack en justifiant son choix et en couvrant les exigences sémantiques.

## Étapes de travail

1. Définir le périmètre, les utilisateurs et les questions auxquelles l’application répondra.
2. Sélectionner et auditer au moins trois sources hétérogènes.
3. Concevoir l’ontologie, les propriétés et la stratégie d’URI en réutilisant des vocabulaires pertinents.
4. Transformer les données en RDF et conserver leur provenance.
5. Installer et configurer un triple store.
6. Écrire et documenter les requêtes SELECT, ASK et CONSTRUCT utiles.
7. Construire le backend et l’interface de recherche, de consultation et de navigation.
8. Publier les métadonnées et les liens vers les sources.
9. Valider les données, requêtes, parcours, URI et cas incomplets.
10. Préparer une installation reproductible, la documentation et une démonstration.

## Questions de validation pour l’équipe

- Quelles ressources et quels utilisateurs sont dans le périmètre ?
- Quelles sources alimentent le graphe, et sous quelles licences ?
- Comment les URI, classes, propriétés et rapprochements sont-ils définis ?
- Quelle fonctionnalité dépend réellement de relations sémantiques ?
- Quelle inférence RDFS/OWL peut être démontrée ?
- Comment la provenance et la qualité sont-elles suivies ?
- Quelles sont les limites connues et les extensions envisagées ?
