---
title: Relationships, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
ms.localizationpriority: medium
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Stocke les relations entre les conteneurs, les listes, les légendes et les formes.
ms.openlocfilehash: 43c07585d9d057a57db9df342c3d7df35b0bafd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607835"
---
# <a name="relationships-cell-shape-layout-section"></a>Relationships, cellule (section Shape Layout)

Stocke les relations entre les conteneurs, les listes, les légendes et les formes. 
  
## <a name="remarks"></a>Remarques

 Microsoft Visio la cellule Relationships pour stocker les relations qui impliquent cette forme. Une série de fonctions DEPENDSON, avec les paramètres affichés, est utilisée pour représenter les relations avec cette forme, comme l’illustre le tableau suivant. 
  
|**Premier paramètre**|**Paramètres supplémentaires**|
|:-----|:-----|
|1  <br/> |Formes membres de ce conteneur.  <br/> |
|2  <br/> |Formes membres de cette liste.  <br/> |
|3  <br/> |Légendes associées à cette forme.  <br/> |
|4   <br/> |Conteneurs dont cette forme est membre.  <br/> |
|5  <br/> |Liste dont cet élément de liste est membre.  <br/> |
|6   <br/> |Forme associée à cette légende.  <br/> |
|7   <br/> |Conteneur sur le bord de la limite gauche sur laquelle réside la forme.  <br/> |
|8   <br/> |Conteneur sur le bord de la limite droite sur laquelle réside la forme.  <br/> |
|9   <br/> |Conteneur sur le bord de la limite haute sur laquelle réside la forme.  <br/> |
|10  <br/> |Conteneur sur le bord de la limite basse sur laquelle réside la forme.  <br/> |
|11  <br/> |Liste sur laquelle chevauche cette liste.  <br/> |
   
Pour obtenir une référence à la cellule Relationships par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Relations  <br/> |
   
Pour obtenir une référence à la cellule Relationships à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLORelationships** <br/> |
   

