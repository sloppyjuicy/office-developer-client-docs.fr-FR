---
title: Propriété canonique PidTagDeltaX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeltaX
api_type:
- HeaderDef
ms.assetid: 9bbe996b-1cfc-46d7-bb0a-291c760500ef
description: Contient la largeur d’un contrôle de boîte de dialogue en unités Windows dialogue standard. Il s’agit de l’une des propriétés qui déterminent la position et la taille de la boîte de dialogue.
ms.openlocfilehash: ca61544db6f2af4f269e3279a2682622403e67a8
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764348"
---
# <a name="pidtagdeltax-canonical-property"></a>Propriété canonique PidTagDeltaX

**S’applique à** : Outlook 2013 | Outlook 2016
  
Contient la largeur d’un contrôle de boîte de dialogue en unités Windows dialogue standard.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DELTAX  <br/> |
|Identificateur :  <br/> |0x3F03  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tableau d’affichage MAPI  <br/> |

## <a name="remarks"></a>Remarques

Les **propriétés PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md)), **PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md)), **PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md)) et cette propriété contrôlent la position et la taille du contrôle de boîte de dialogue.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.

Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.

## <a name="see-also"></a>Voir aussi

[Propriétés MAPI](mapi-properties.md)  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
