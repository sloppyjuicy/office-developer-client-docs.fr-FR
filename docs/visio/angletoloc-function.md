---
title: ANGLETOLOC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
ms.localizationpriority: medium
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Renvoie un angle transformé dans le système de coordonnées locales de la forme de destination. Convertit un angle de coordonnées locales de la forme source en coordonnées locales de la forme de destination.
ms.openlocfilehash: f735535cec34dc81c3e80a47939eee6a1584d51a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783718"
---
# <a name="angletoloc-function"></a>Fonction ANGLETOLOC

Renvoie un angle transformé dans le système de coordonnées locales de la forme de destination. Convertit un angle de coordonnées locales de la forme source en coordonnées locales de la forme de destination. 
    
 
  
## <a name="syntax"></a>Syntaxe

ANGLETOLOC(***srcAngle** _, _*_srcRef_*_, _ *_dstRef_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Requis  <br/> |**Numérique** <br/> |Angle dans le système de coordonnées source. |
| _srcRef_ <br/> |Requis  <br/> |**String** <br/> | Référence à une cellule de l’objet source, comme une forme, un groupe, une page, etc. |
| _dstRef_ <br/> |Requis  <br/> |**String** <br/> |Référence à une cellule de l’objet de destination, comme une forme, un groupe, une page, etc. |
   
## <a name="remarks"></a>Remarques

La fonction ANGLETOLOC permet de définir les cellules d’angle local d’une forme en termes d’angle d’un autre espace de coordonnées.
  
Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.
  
Les coordonnées source et cible doivent se trouver sur la même page.
  

