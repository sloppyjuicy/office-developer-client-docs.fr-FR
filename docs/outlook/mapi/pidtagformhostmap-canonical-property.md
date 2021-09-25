---
title: Propriété canonique PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8c7869e6bcfc926e071b386cc70f446b537ac28
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587677"
---
# <a name="pidtagformhostmap-canonical-property"></a>Propriété canonique PidTagFormHostMap

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une carte hôte des formulaires disponibles. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FORM_HOST_MAP  <br/> |
|Identificateur :  <br/> |0x3306  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |MAPI courant  <br/> |
   
## <a name="remarks"></a>Remarques

Une application cliente doit mettre à jour cette propriété, ainsi que la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), lors de la modification de la structure sous-jacente dans l’interface **IMAPIFormProp.** 
  
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

