---
title: Cahier des charges Web
weight: 1
description: >
  Produire des sites et services Web éco-conçus, accessibles aux personnes en situation de handicap, utiles, utilisables et utilisés.

---

{{< callout emoji="💬" >}}
Ce cahier des charges vise à proposer une base saine pour un projet numérique de site ou de service numérique. Dans l'ensemble du document, nous utiliserons "Le site" pour parler du livrable, mais ce terme peut être adapté en fonction de la spécificité du contexte. 

Les chapitres encadrés tels que celui-ci fournissent des informations de contexte à l'organisation qui souhaite utiliser le cahier des charges. Ils peuvent être supprimés du document final.
{{< /callout >}}

{{% details title="Pour en savoir plus" closed="true" %}}
En encadré comme ceci, les sources et références.
{{% /details %}}

## Contexte [C]

{{< callout emoji="💬" >}}
Les personnes qui répondent à votre appel d'offres ont besoin de comprendre qui vous êtes, et quel problème vous voulez résoudre. Pour cela, il faut une information juste, sincère et suffisante. Et il faut éviter de noyer sous un volume important d'informations non pertinentes
{{< /callout >}}

### Organisation

### Projet

### Système d'information existant

### Cadre légal spécifique

## Méthodologie [M]

{{< callout emoji="💬" >}}
Un projet Web s'adresse toujours à des usagers. Gérer un projet Web sans intégrer les utilisateurs, c'est un peu comme le jeu de la piñata : on ne sait pas ce qui va marcher ou pas, parce qu'on ne voit rien. Ça peut finir par marcher, mais [ce n'est pas très efficace](https://siecledigital.fr/2022/08/26/sncf-connect-un-fiasco-a-50-millions-deuros/).
{{< /callout >}}

### Co-construction avec les usagers

Exploration, priorisation

### Tests utilisateurs

Aux phases de maquette, pré-production, et production.
## Fonctionnalités [F]

### Impératifs

### Possibilités
## Exigences techniques [T]

{{< callout emoji="💬" >}}
Un projet numérique induit une couche technique, qui a forcément un impact multi-factoriel. Il s'agit ici de qualifier l'impact, de définir un principe "minimal par défaut" et de fixer un cadre chiffré d'objectifs à atteindre ou à ne pas dépasser.
{{< /callout >}}

Le numérique étant à la fois matériel (impact écologique) et excluant (impact sociétal), il est nécessaire de faire des choix techniques pertinents, à même de minimiser l'impact écologique et de maximiser l'accessibilité, tout en garantissant le parfait respect des données personnelles, la souveraineté opérationnelle et en assurant la pérennité de la solution.

L'ensemble des choix techniques préconisés devront l'être en respectant le principe du "minimal par défaut", c'est à dire que la solution la plus simple techniquement doit être envisagée comme base, et chaque brique technique ajoutée doit l'être à la suite d'une analyse bénéfices/risques favorable. La préconisation d'une solution "parce qu'elle fonctionne bien" ou "parce qu'elle est bien maîtrisée" génère des sous-optimalités à tous les niveaux.

{{% details title="Pour en savoir plus" closed="true" %}}
- [Numérique, éducation et cosmopolitisme](https://www.cairn.info/revue-cites-2015-3-page-13.htm)
{{% /details %}}

### Accessibilité [TA]

### Écoconception [TE]

{{< callout emoji="💬" >}}
Dans le contexte d'un site Web, l'écoconception commence par questionner le besoin de numérisation : a-t-on vraiment besoin d'un site ? Peut-on faire sans ? Ce besoin doit être interrogé avec les usagers, dans la partie [P]. Si le besoin est avéré, ce chapitre va permettre de fixer des conditions cibles qui minimiseront l'impact du site.
{{< /callout >}}

Comme défini par la DINUM, les objectifs de l'écoconception de services numériques sont de réduire la consommation de ressources informatiques et énergétiques et la contribution à l’obsolescence des équipements, qu’il s’agisse des équipements utilisateurs ou des équipements réseau ou serveur. 

Le site doit avoir l'impact écologique le plus léger possible, sur plusieurs niveaux :
- minimisation de l'impact serveur
- minimisation de l'impact réseau
- minimisation de l'impact périphérique

{{% details title="Pour en savoir plus" closed="true" %}}
- [Référentiel général d'écoconception de services numériques (RGESN)](https://ecoresponsable.numerique.gouv.fr/publications/referentiel-general-ecoconception/)
- [GR491](https://gr491.isit-europe.org/)
{{% /details %}}

#### Minimisation de l'impact serveur [TEV]
{{< callout emoji="💬" >}}
Une cause importante de charge côté serveur est d'utiliser une solution identique pour tous les usages, comme par exemple WordPress. La solution doit être choisie en fonction des besoins réels, pas seulement parce que l'équipe qui la met en œuvre la connaît bien.
{{< /callout >}}

La charge de calcul et de stockage sur les serveurs doit être aussi légère que possible. 
Pour cela, les choix architecturaux devront être justifiés, en partant du cas le plus simple, à savoir les fichiers HTML bruts, précompilés.
Chaque composant logiciel ajouté (base de données, CMS, framework...) devra faire l'objet d'une analyse bénéfices/risques, et d'une preuve que la solution plus simple n'est pas adaptée au cas d'usage.

Les données doivent être stockées de la façon la plus légère possible sans empêcher leur usage. 
Le fonctionnement "par défaut" est de ne conserver aucune donnée.
Chaque donnée doit être conservée uniquement par rapport à un usage défini au préalable, clairement identifié et proportionné aux besoins.

Les traitements de données pouvant nécessiter des calculs intensifs, par exemple les préparations d'images pour différents formats d'affichage, doivent être exécutés une et une seule fois, en fonction du besoin réel. Les solutions de génération différée (lazy loading) mise en cache seront privilégiées par rapport aux solutions de génération lors de l'envoi (qui impliquent des calculs potentiellement inutiles) et surtout par rapport à la génération à la volée sans système de cache (qui impliquent des recalculs à l'identique).

L'infrastructure d'hébergement choisie doit présenter les meilleurs preuves d'efficacité, tant sur l'usage de l'électricité (Power Usage Effectiveness, PUE) que sur l'usage de l'eau (Water Usage Effectiveness, WUE). L'équilibre doit être recherché entre la souveraineté, la performance technique et la sobriété.

{{% details title="Pour en savoir plus" closed="true" %}}
- [RGESN Backend](https://ecoresponsable.numerique.gouv.fr/publications/referentiel-general-ecoconception/#backend)
- [RGESN Hébergement](https://ecoresponsable.numerique.gouv.fr/publications/referentiel-general-ecoconception/#hebergement)
{{% /details %}}

#### Minimisation de l'impact réseau [TER]
{{< callout emoji="💬" >}}
Les pages très lourdes ont plusieurs causes classiques, notamment les vidéos, les images et les librairies techniques. Des techniques existent pour diminuer ces impacts, encore faut-il définir précisément les attentes.
{{< /callout >}}

Les pages doivent être légères, particulièrement en mobile :
- les images seront chargées en utilisant des formats adaptés (picture et srcset), redimensionnés du côté du serveur
- le poids total téléchargé sur mobile, sans naviguer, sera à l'idéal inférieur à 500 ko, au pire inférieur à 1 mo
- aucune vidéo ne démarrera automatiquement (autoplay) 
- le nombre de requêtes par page sera à l'idéal inférieur à 25, au pire inférieur à 50
- la politique de cache permettra d'éviter les rechargements inutiles, d'une page sur l'autre et d'une visite sur l'autre

{{% details title="Pour en savoir plus" closed="true" %}}
- [Core Web Vitals](https://web.dev/learn-core-web-vitals/)
- [Fast load times](https://web.dev/fast/)
- [Reduce HTTP Requests Like a Pro & Boost Your Site Speed](https://www.titangrowth.com/blog/reduce-http-requests-like-a-pro-120/)
{{% /details %}}

#### Minimisation de l'impact périphérique [TEP]

Rétrocompatibilité

Par défaut pas de framework, tout à justifier (bénéfices/risques)

### Respect des données personnelles

### Souveraineté de l'infrastructure

#### Minimisation des dépendances techniques

#### Choix de l'hébergement

### Pérennité technique

## Exigences légales [L]

### Conformité RGAA

### Conformité RGESN

### Conformité RGPD

## Prix [P]

### Rémunération de l'appel d'offres

### Prix du marché

### Critères de décision