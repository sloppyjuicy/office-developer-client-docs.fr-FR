---
title: Propriété canonique PidTagScheduleInfoAutoAcceptAppointments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4f2cab31d6eed19a262bd0e667166bc79f428877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786694"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a>Propriété canonique PidTagScheduleInfoAutoAcceptAppointments

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si un client ou serveur doit répondre automatiquement à toutes les demandes de réunion pour la ressource ou un participant.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_AUTO_ACCEPT_APPTS  <br/> |
|Identificateur :  <br/> |0x686D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Lors de la réponse, la réponse doit être acceptation, sauf si pour une contrainte supplémentaire qui est spécifiée par la **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) ou **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** propriétés ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) est remplie. La valeur FALSE ou l’absence de cette propriété indique qu’un client ou serveur ne doit pas accepter automatiquement les demandes de réunion. Il n’est pas une propriété requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou une ressource.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

