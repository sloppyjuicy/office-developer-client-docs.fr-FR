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
ms.openlocfilehash: 357ba47fd28b869068d2c28f35df1406909105ff
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521448"
---
# <a name="relationships-cell-shape-layout-section"></a>Relationships, cellule (section Shape Layout)

Stocke les relations entre les conteneurs, les listes, les légendes et les formes. 
  
## <a name="remarks"></a>Remarques

 Microsoft Visio la cellule Relationships pour stocker les relations qui impliquent cette forme. Une série de fonctions DEPENDSON, avec les paramètres affichés, est utilisée pour représenter les relations avec cette forme, comme l’illustre le tableau suivant. 
  
|**Premier paramètre**|**Paramètres supplémentaires**|
|:-----|:-----|
|1  <br/> |Formes membres de ce conteneur. |
|2  <br/> |Formes membres de cette liste. |
|3  <br/> |Légendes associées à cette forme. |
|4  <br/> |Conteneurs dont cette forme est membre. |
|5  <br/> |Liste dont cet élément de liste est membre. |
|6   <br/> |Forme associée à cette légende. |
|7   <br/> |Conteneur sur le bord de la limite gauche sur laquelle réside la forme. |
|8   <br/> |Conteneur sur le bord de la limite droite sur laquelle réside la forme. |
|9   <br/> |Conteneur sur le bord de la limite haute sur laquelle réside la forme. |
|10  <br/> |Conteneur sur le bord de la limite basse sur laquelle réside la forme. |
|11  <br/> |Liste sur laquelle chevauche cette liste. |
   
Pour obtenir une référence à la cellule Relationships par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Relations  <br/> |
   
Pour obtenir une référence à la cellule Relationships à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowShapeLayout** <br/> |
|**Index de la cellule :**  <br/> |**visSLORelationships** <br/> |
   

