---
title: Cahier des charges Web
---

> Ce cahier des charges vise à proposer une base saine pour un projet numérique de site ou de service numérique. Dans l'ensemble du document, nous utiliserons "Le site" pour parler du livrable, mais ce terme peut être adapté en fonction de la spécificité du contexte. 

> Les chapitres tels que celui-ci, signalés par un trait orange, fournissent des informations de contexte à l'organisation qui souhaite utiliser le cahier des charges. Ils peuvent être supprimés du document final.

## Contexte [C]

### Organisation

### Projet

### Système d'information existant

### Cadre légal spécifique

## Exigences projet [P]

### Méthodologie intégrant les usagers
 
## Exigences fonctionnelles [F]

### Impératifs

### Possibilités
## Exigences techniques [T]
### Accessibilité [TA]

### Écoconception [TE]

> Dans le contexte d'un site Web, l'écoconception commence par questionner le besoin de numérisation : a-t-on vraiment besoin d'un site ? Peut-on faire sans ? Ce besoin doit être interrogé avec les usagers, dans la partie [P]. Si le besoin est avéré, ce chapitre va permettre de fixer des conditions cibles qui minimiseront l'impact du site.

Comme défini par la DINUM, les objectifs de l'écoconception de services numériques sont de réduire la consommation de ressources informatiques et énergétiques et la contribution à l’obsolescence des équipements, qu’il s’agisse des équipements utilisateurs ou des équipements réseau ou serveur. 

Le site doit avoir l'impact écologique le plus léger possible, sur plusieurs niveaux :
- minimisation de l'impact serveur
- minimisation de l'impact réseau
- minimisation de l'impact périphérique

Sources et références :
- [Référentiel général d'écoconception de services numériques (RGESN)](https://ecoresponsable.numerique.gouv.fr/publications/referentiel-general-ecoconception/)
- [GR491](https://gr491.isit-europe.org/)

#### Minimisation de l'impact serveur [TEV]

#### Minimisation de l'impact réseau [TER]
> Les pages très lourdes ont plusieurs causes classiques, notamment les vidéos, les images et les librairies techniques. Des techniques existent pour diminuer ces impacts, encore faut-il définir précisément les attentes.

Les pages doivent être légères, particulièrement en mobile :
- les images seront chargées en utilisant des formats adaptés (picture et srcset), redimensionnés du côté du serveur
- le poids total téléchargé sur mobile, sans naviguer, sera à l'idéal inférieur à 500 ko, au pire inférieur à 1 mo
- aucune vidéo ne démarrera automatiquement (autoplay) 
- le nombre de requêtes par page sera à l'idéal inférieur à 25, au pire inférieur à 50
- la politique de cache permettra d'éviter les rechargements inutiles, d'une page sur l'autre et d'une visite sur l'autre

Sources et références :
- [Core Web Vitals](https://web.dev/learn-core-web-vitals/)
- [Fast load times](https://web.dev/fast/)
- [Reduce HTTP Requests Like a Pro & Boost Your Site Speed](https://www.titangrowth.com/blog/reduce-http-requests-like-a-pro-120/)
#### Minimisation de l'impact périphérique [TEP]


### Respect des données personnelles

### Souveraineté de l'infrastructure

#### Minimisation des dépendances techniques

## Exigences légales [L]

### Conformité RGAA

### Conformité RGESN

### Conformité RGPD