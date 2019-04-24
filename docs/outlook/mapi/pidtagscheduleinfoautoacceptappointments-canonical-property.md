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
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330092"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a>Propriété canonique PidTagScheduleInfoAutoAcceptAppointments

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si un client ou un serveur doit répondre automatiquement à toutes les demandes de réunion pour le participant ou la ressource.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_AUTO_ACCEPT_APPTS  <br/> |
|Identificateur :  <br/> |0x686D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Lors de la réponse, la réponse doit être acceptée, sauf si une contrainte supplémentaire est spécifiée par **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) ou **PR_SCHDINFO_DISALLOW_ **Les propriétés OVERLAPPING_APPTS ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) sont remplies. La valeur FALSe ou l'absence de cette propriété indique qu'un client ou un serveur ne doit pas accepter automatiquement les demandes de réunion. Cette propriété n'est pas obligatoire.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d'un utilisateur ou d'une ressource.
    
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

