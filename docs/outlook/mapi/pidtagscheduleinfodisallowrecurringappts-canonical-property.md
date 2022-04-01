---
title: Propriété canonique PidTagScheduleInfoDisallowRecurringAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: Contient TRUE lorsque la réponse automatique aux rendez-vous périodiques est refusée. Cette propriété n’est significative que lorsque la valeur de PR_SCHDINFO_AUTO_ACCEPT_APPTS est TRUE.
ms.openlocfilehash: a0a7b12f29c0b99527f01f0da75e41e8f176d36a
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524387"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a>Propriété canonique PidTagScheduleInfoDisallowRecurringAppts

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE lorsque la réponse automatique aux rendez-vous périodiques est refuser.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_DISALLOW_RECURRING_APPTS  <br/> |
|Identificateur :  <br/> |0x686E  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est significative que lorsque la valeur de la **propriété PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) est TRUE. L’absence de cette propriété indique que les réunions périodiques doivent être acceptées. Il ne s’agit pas d’une propriété obligatoire.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou d’une ressource.
    
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

