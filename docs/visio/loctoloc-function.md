---
title: LOCTOLOC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Renvoie un point transformé en coordonnées locales dans le système de coordonnées de destination.
ms.openlocfilehash: 444200801ebd984fb735b95de6d58d35e5160d1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789050"
---
# <a name="loctoloc-function"></a>LOCTOLOC, fonction

Renvoie un point transformé en coordonnées locales dans le système de coordonnées de destination.
  
## <a name="syntax"></a>Syntaxe

LOCTOLOC (** *pointSrc* **, ** *srcRef* **, ** *dstRef* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _pointSrc_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Point en coordonnées locales du système de coordonnées source  <br/> |
| _srcRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Référence à une cellule de l’objet source  <br/> |
| _dstRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Référence à une cellule de l’objet cible  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction LOCTOLOC convertit un point des coordonnées locales de la forme source en coordonnées locales de la forme de destination. Elle permet, par exemple, de construire une forme en utilisant les points d’un autre système de coordonnées. Elle permet également de transformer un point local en coordonnées de page ou vice-versa.
  
Vous pouvez l’utiliser même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.
  
Les coordonnées source et cible doivent se trouver sur la même page.
  
## <a name="example"></a>Exemple

La formule suivante convertit les coordonnées de l’axe local de la forme associée à la formule en un point de la page.
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


