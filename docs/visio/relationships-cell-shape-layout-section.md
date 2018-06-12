---
title: Relationships, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Stocke les relations entre les conteneurs, les listes, les légendes et les formes.
ms.openlocfilehash: c3410ad15581ff1704d7a43dd7ed5fa193f668b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789430"
---
# <a name="relationships-cell-shape-layout-section"></a>Relationships, cellule (section Shape Layout)

Stocke les relations entre les conteneurs, les listes, les légendes et les formes. 
  
## <a name="remarks"></a>Note

 Microsoft Visio utilise la cellule Relationships pour stocker les relations qui mettent en œuvre cette forme. Une série de fonctions DEPENDSON, avec les paramètres indiqués, sont utilisés pour représenter les relations avec cette forme, comme indiqué dans le tableau suivant. 
  
|**Premier paramètre**|**Paramètres supplémentaires**|
|:-----|:-----|
|1  <br/> |Formes membres de ce conteneur.  <br/> |
|2  <br/> |Formes membres de cette liste.  <br/> |
|3  <br/> |Légendes associées à cette forme.  <br/> |
|4  <br/> |Conteneurs dont cette forme est membre.  <br/> |
|5  <br/> |Liste dont cet élément de liste est membre.  <br/> |
|6  <br/> |Forme associée à cette légende.  <br/> |
|7  <br/> |Conteneur sur le bord de la limite gauche sur laquelle réside la forme.  <br/> |
|8  <br/> |Conteneur sur le bord de la limite droite sur laquelle réside la forme.  <br/> |
|9  <br/> |Conteneur sur le bord de la limite haute sur laquelle réside la forme.  <br/> |
|10  <br/> |Conteneur sur le bord de la limite basse sur laquelle réside la forme.  <br/> |
|11  <br/> |Liste sur laquelle chevauche cette liste.  <br/> |
   
Pour obtenir une référence à la cellule Relationships par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Relations  <br/> |
   
Pour obtenir une référence à la cellule Relationships par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLORelationships** <br/> |
   

