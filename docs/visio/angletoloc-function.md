---
title: ANGLETOLOC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Renvoie un angle transformé dans le système de coordonnées local de la forme de destination. Convertit un angle de coordonnées locales de la forme source en coordonnées locales de la forme de destination.
ms.openlocfilehash: 09ab0a4a55446dd74729f1da0bcf022d8376909b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788023"
---
# <a name="angletoloc-function"></a>ANGLETOLOC, fonction

Renvoie un angle transformé dans le système de coordonnées local de la forme de destination. Convertit un angle de coordonnées locales de la forme source en coordonnées locales de la forme de destination. 
  
## <a name="syntax"></a>Syntaxe

ANGLETOLOC (** *AngleScr* **, ** *srcRef* **, ** *dstRef* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _AngleScr_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Angle dans le système de coordonnées source.  <br/> |
| _srcRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Référence à une cellule de l’objet source, comme une forme, un groupe, une page, etc.  <br/> |
| _dstRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Référence à une cellule de l’objet de destination, comme une forme, un groupe, une page, etc.  <br/> |
   
## <a name="remarks"></a>Note

La fonction ANGLETOLOC permet de définir les cellules d’angle local d’une forme en termes d’angle d’un autre espace de coordonnées.
  
Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.
  
Les coordonnées source et cible doivent se trouver sur la même page.
  

