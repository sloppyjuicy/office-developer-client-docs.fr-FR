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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330085"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a>Propriété canonique PidTagScheduleInfoDisallowOverlappingAppts

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si les rendez-vous qui se chevauchent ne sont pas autorisés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS  <br/> |
|Identificateur :  <br/> |0x686F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n'a de sens que si la valeur de la propriété **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PIDTAGSCHEDULEINFOAUTOACCEPTAPPOINTMENTS](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) est true. La valeur TRUE indique que lors de la réponse automatique aux demandes de réunion, un client ou un serveur doit refuser les instances qui chevauchent les événements planifiés précédemment. La valeur FALSe ou l'absence de cette propriété indique que les instances qui se chevauchent doivent être acceptées. Cette propriété n'est pas obligatoire.
  
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

