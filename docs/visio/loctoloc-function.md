---
title: LOCTOLOC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
ms.localizationpriority: medium
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Renvoie un point transformé en coordonnées locales dans le système de coordonnées de destination.
ms.openlocfilehash: 69923fe5aac909043449ed01d0046bbe06242bd8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62786796"
---
# <a name="loctoloc-function"></a>Fonction LOCTOLOC

Renvoie un point transformé en coordonnées locales dans le système de coordonnées de destination.
  
## <a name="syntax"></a>Syntaxe

LOCTOLOC(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Requis  <br/> |**String** <br/> | Point en coordonnées locales du système de coordonnées source |
| _srcRef_ <br/> |Requis  <br/> |**String** <br/> | Référence à une cellule de l’objet source |
| _dstRef_ <br/> |Requis  <br/> |**String** <br/> | Référence à une cellule de l’objet cible |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction LOCTOLOC convertit un point des coordonnées locales de la forme source en coordonnées locales de la forme de destination. Elle permet, par exemple, de construire une forme en utilisant les points d’un autre système de coordonnées. Elle permet également de transformer un point local en coordonnées de page ou vice-versa.
  
Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.
  
Les coordonnées source et cible doivent se trouver sur la même page.
  
## <a name="example"></a>Exemple

La formule suivante convertit les coordonnées de l’axe local de la forme associée à la formule en un point de la page.
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


