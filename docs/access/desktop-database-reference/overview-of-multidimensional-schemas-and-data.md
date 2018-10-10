---
title: Présentation des schémas et données multidimensionnels
TOCTitle: Overview of Multidimensional Schemas and Data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef416e62d17b5b4821b5051ecc59cc6e0dfb5739
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471933"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>Présentation des schémas et données multidimensionnels


**S’applique à**: Access 2013 | Office 2013

## <a name="understanding-multidimensional-schemas"></a>Présentation des schémas multidimensionnels

Dans ADO MD, l'objet de métadonnées central est le *cube*, qui consiste en un ensemble structuré de dimensions, hiérarchies, niveaux et membres connexes.

Une *dimension* est une catégorie indépendante de données à partir de votre base de données multidimensionnelle sur vos entités professionnelles. En règle générale, une dimension contient les éléments à utiliser comme critères de requête pour les mesures de la base de données.

Une *hiérarchie* est un chemin d’agrégation dans une dimension. Une dimension peut avoir plusieurs niveaux de granularité dotés de relations parent-enfant. Une hiérarchie permet de définir les relations entre ces niveaux.

Un *niveau* est une étape d’agrégation dans une hiérarchie. Pour les dimensions dotées de plusieurs couches d'informations, chaque couche constitue un niveau.

Un *membre* est un élément de données dans une dimension. En règle générale, vous créez une légende ou décrivez une mesure de la base de données à l'aide de membres.

Les cubes sont représentés par des objets [CubeDef](cubedef-object-ado-md.md) dans ADO MD. Les dimensions, hiérarchies, niveaux et membres sont également représentés par leurs objets ADO MD correspondants : [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) et [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensions

Les dimensions d'un cube dépendent de vos entités professionnelles et des types de données à représenter dans la base de données. En règle générale, chaque dimension constitue un point d'entrée ou un mécanisme indépendant permettant de sélectionner des données.

Par exemple, un cube contenant des données de ventes possède les cinq dimensions suivantes : Vendeur, Géographie, Heure, Produits et Mesures. La dimension Mesures contient les valeurs de données de ventes réelles tandis que les autres dimensions constituent des manières de classer et regrouper les valeurs des données de ventes.

La dimension Géographie est constituée des membres suivants :

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hiérarchies

Les hiérarchies définissent les manières de regrouper ou de reporter les niveaux d'une dimension. Une dimension peut compter plusieurs hiérarchies.

## <a name="levels"></a>Niveaux

Dans l'exemple de la dimension Géographie de l'illustration précédente, chaque zone représente un niveau de la hiérarchie.

Chaque niveau est constitué de membres, comme suit :

  - Monde = {All}


  - Continents = {North America, Europe}


  - Pays = {Canada, USA, UK, Germany}


  - Régions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


  - Villes = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>Membres

Les membres inférieurs d'une hiérarchie n'ont pas d'enfants et les membres supérieurs n'ont pas de parents. Tous les autres membres ont au moins un parent et un enfant. Par exemple, une coupure transversale de l'arborescence hiérarchique de la dimension Géographie donne les relations parent-enfant suivantes :

  - {All} (parent) {Europe, Amérique du Nord}

  - {Amérique du Nord} (parent) {Canada, USA}

  - {USA} (parent) {USA-NE, USA-NW, USA-SE, USA-SW}

  - {USA-NW} (parent) {Seattle, Boise}

Les membres peuvent faire partie d'une ou plusieurs hiérachies par dimension.

Cet exemple illustre également une autre caractéristique : certains membres du niveau Semaine de la hiérarchie Année-Semaine n'apparaissent dans aucun niveau de la hiérarchie Année-Trimestre. Autrement dit, une hiérarchie ne doit pas nécessairement comprendre tous les membres d'une dimension.

## <a name="understanding-multidimensional-schemas"></a>Présentation des schémas multidimensionnels

Dans ADO MD, l'objet de métadonnées central est le *cube*, qui consiste en un ensemble structuré de dimensions, hiérarchies, niveaux et membres connexes.

Une *dimension* est une catégorie indépendante de données à partir de votre base de données multidimensionnelle sur vos entités professionnelles. En règle générale, une dimension contient les éléments à utiliser comme critères de requête pour les mesures de la base de données.

Une *hiérarchie* est un chemin d’agrégation dans une dimension. Une dimension peut avoir plusieurs niveaux de granularité dotés de relations parent-enfant. Une hiérarchie permet de définir les relations entre ces niveaux.

Un *niveau* est une étape d’agrégation dans une hiérarchie. Pour les dimensions dotées de plusieurs couches d'informations, chaque couche constitue un niveau.

Un *membre* est un élément de données dans une dimension. En règle générale, vous créez une légende ou décrivez une mesure de la base de données à l'aide de membres.

Les cubes sont représentés par des objets [CubeDef](cubedef-object-ado-md.md) dans ADO MD. Les dimensions, hiérarchies, niveaux et membres sont également représentés par leurs objets ADO MD correspondants : [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) et [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensions

Les dimensions d'un cube dépendent de vos entités professionnelles et des types de données à représenter dans la base de données. En règle générale, chaque dimension constitue un point d'entrée ou un mécanisme indépendant permettant de sélectionner des données.

Par exemple, un cube contenant des données de ventes possède les cinq dimensions suivantes : Vendeur, Géographie, Heure, Produits et Mesures. La dimension Mesures contient les valeurs de données de ventes réelles tandis que les autres dimensions constituent des manières de classer et regrouper les valeurs des données de ventes.

La dimension Géographie est constituée des membres suivants :

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hiérarchies

Les hiérarchies définissent les manières de regrouper ou de reporter les niveaux d'une dimension. Une dimension peut compter plusieurs hiérarchies.

## <a name="levels"></a>Niveaux

Dans l'exemple de la dimension Géographie de l'illustration précédente, chaque zone représente un niveau de la hiérarchie.

Chaque niveau est constitué de membres, comme suit :

- Monde = {All}


- Continents = {North America, Europe}


- Pays = {Canada, USA, UK, Germany}


- Régions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


- Villes = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>Membres

Les membres inférieurs d'une hiérarchie n'ont pas d'enfants et les membres supérieurs n'ont pas de parents. Tous les autres membres ont au moins un parent et un enfant. Par exemple, une coupure transversale de l'arborescence hiérarchique de la dimension Géographie donne les relations parent-enfant suivantes :

- {All} (parent) {Europe, Amérique du Nord}

- {Amérique du Nord} (parent) {Canada, USA}

- {USA} (parent) {USA-NE, USA-NW, USA-SE, USA-SW}

- {USA-NW} (parent) {Seattle, Boise}

Les membres peuvent faire partie d'une ou plusieurs hiérachies par dimension.

Cet exemple illustre également une autre caractéristique : certains membres du niveau Semaine de la hiérarchie Année-Semaine n'apparaissent dans aucun niveau de la hiérarchie Année-Trimestre. Autrement dit, une hiérarchie ne doit pas nécessairement comprendre tous les membres d'une dimension.

