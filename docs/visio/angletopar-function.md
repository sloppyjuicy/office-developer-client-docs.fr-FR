---
title: ANGLETOPAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Renvoie un angle transformé dans le système de coordonnées parent de la forme de destination. Convertit un angle des coordonnées locales de la forme source en coordonnées parent de la forme de destination.
ms.openlocfilehash: 0fed51e264bfb21da25d4e91f20f4bc0803e46e8
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160257"
---
# <a name="angletopar-function"></a>Fonction ANGLETOPAR

Renvoie un angle transformé dans le système de coordonnées parent de la forme de destination. Convertit un angle des coordonnées locales de la forme source en coordonnées parent de la forme de destination. 
  
## <a name="syntax"></a>Syntaxe

ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** ) 
  
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
  

