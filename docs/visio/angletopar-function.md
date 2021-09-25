---
title: ANGLETOPAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
ms.localizationpriority: medium
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Renvoie un angle transformé dans le système de coordonnées parent de la forme de destination. Convertit un angle des coordonnées locales de la forme source en coordonnées parent de la forme de destination.
ms.openlocfilehash: 15be3a0230f439221b1d6a20be63abd456acc4cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603920"
---
# <a name="angletopar-function"></a>Fonction ANGLETOPAR

Renvoie un angle transformé dans le système de coordonnées parent de la forme de destination. Convertit un angle des coordonnées locales de la forme source en coordonnées parent de la forme de destination.
    
 
  
## <a name="syntax"></a>Syntaxe

ANGLETOPAR(***srcAngle** _, _*_srcRef_*_, _ *_dstRef_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Angle dans le système de coordonnées source.  <br/> |
| _srcRef_ <br/> |Obligatoire  <br/> |**String** <br/> | Référence à une cellule de l’objet source, comme une forme, un groupe, une page, etc.  <br/> |
| _dstRef_ <br/> |Obligatoire  <br/> |**String** <br/> |Référence à une cellule de l’objet de destination, comme une forme, un groupe, une page, etc.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.
  
Les coordonnées source et cible doivent se trouver sur la même page.
  
Si la destination est une page, qui n’a pas de parent, le résultat est exprimé dans les coordonnées locales de la page.
  

