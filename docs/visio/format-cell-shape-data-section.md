---
title: Format, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251340
localization_priority: Normal
ms.assetid: c36fc895-5577-59f6-0ff5-5892ca81a58f
description: Définit la mise en forme d'un élément de données de forme qui est une chaîne, une liste fixe, un nombre, une liste variable, une date, une heure ou une monnaie.
ms.openlocfilehash: 48342f21a107ff78fed2347fb679ed8199526056
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788704"
---
# <a name="format-cell-shape-data-section"></a>Format, cellule (section Shape Data)

Définit la mise en forme d'un élément de données de forme qui est une chaîne, une liste fixe, un nombre, une liste variable, une date, une heure ou une monnaie.
  
## <a name="remarks"></a>Notes

|**Type d’élément de données de forme**|**Valeur**|**Contenu de la cellule Format**|
|:-----|:-----|:-----|
| Chaîne  <br/> | 0  <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Liste fixe  <br/> | 1  <br/> | Éléments de la liste, séparés par des signes deux-points.  <br/> |
| Nombre  <br/> | 2  <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Liste variable  <br/> | 4  <br/> | Éléments de la liste, séparés par des signes deux-points.  <br/> |
| Date ou heure  <br/> | 5  <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Durée  <br/> | 6  <br/> | Modèle de format approprié pour le type de données.  <br/> |
| Devise  <br/> | 7  <br/> | Modèle de format approprié pour le type de données.  <br/> |
   
Un exemple de modèle de format approprié pour le type de données, le format image « # #/ 4 UU » met en forme les numéros de 12,43 ;. en tant que 12 2/4 pouces. Pour plus d’informations sur la spécification d’un format de l’image, voir [à propos des modèles de format](about-format-pictures.md).
  
Un exemple d'éléments spécifiés pour une liste est « Ingénierie;Ressources humaines;Ventes;Marketing ».
  
Les valeurs de date (type = 5) sont affichés dans le format de date court. Les valeurs monétaires (type = 7) sont affichés à l’aide du paramètre actuel de l’utilisateur pour la **devise** sous l’onglet **Options régionales** dans l’élément **Options régionales et linguistiques** dans **Le panneau de configuration**.
  
Un nombre (type = 2) peut représenter une cote, un vecteur, un angle, une date, une heure ou une devise. Pour vous assurer qu'un nombre entré est toujours évalué comme une date, une heure ou une devise, utilisez la fonction DATEHEURE ou CY dans la cellule Format au lieu d'un modèle de format.
  
Pour obtenir une référence à la cellule Format par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Propriétés.  *nom* . Format dans lequel de propriétés.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Format par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsFormat** <br/> |
   

