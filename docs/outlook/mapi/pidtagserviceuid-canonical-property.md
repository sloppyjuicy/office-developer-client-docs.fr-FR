---
title: Propriété canonique PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786799"
---
# <a name="pidtagserviceuid-canonical-property"></a>Propriété canonique PidTagServiceUid

  
  
**S’applique à**: Outlook 
  
Contient la structure [MAPIUID](mapiuid.md) d’un service de message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_UID  <br/> |
|Identificateur :  <br/> |0x3D0C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est calculée par MAPI sur les objets section de profil. MAPI utilise pour tous les fournisseurs qui appartiennent au même service de message de groupe. Cette propriété est fournie en tant que paramètre à la plupart des méthodes [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Il ne doit pas apparaître dans le fichier Mapisvc.inf. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

