---
title: Propriété canonique PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316225"
---
# <a name="pidtagformhostmap-canonical-property"></a>Propriété canonique PidTagFormHostMap

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une carte hôte des formulaires disponibles. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FORM_HOST_MAP  <br/> |
|Identificateur :  <br/> |0x3306  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Une application cliente doit mettre à jour cette propriété, ainsi que la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), lors de la modification de la structure sous-jacente dans l'interface **IMAPIFormProp** . 
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

