---
title: Propriété canonique PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391898"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a>Propriété canonique PidTagScheduleInfoDisallowOverlappingAppts

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si le rendez-vous qui se chevauchent ne sont pas autorisés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS  <br/> |
|Identificateur :  <br/> |0x686F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est explicite uniquement lorsque la valeur de la propriété **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) a la valeur TRUE. La valeur TRUE indique que lorsque vous répondez automatiquement aux demandes de réunion, un client ou serveur doit refuser instances qui se chevauchent événements planifiées auparavant. La valeur FALSE ou l’absence de cette propriété indique que le chevauchement des instances doit être accepté. Il n’est pas une propriété requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou une ressource.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

