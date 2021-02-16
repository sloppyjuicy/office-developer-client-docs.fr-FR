---
title: Propriété canonique PidTagRecipientProposedEndTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332773"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a>Propriété canonique PidTagRecipientProposedEndTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’heure de fin proposée d’une réunion.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_PROPOSEDENDTIME  <br/> |
|Identificateur :  <br/> |0x5FE4  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Destinataire de transport  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque la valeur de la propriété **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) est définie sur TRUE, la valeur de cette propriété indique la valeur demandée par le participant à définir comme valeur de la propriété **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) pour l’objet de réunion ou l’objet d’exception d’instance unique.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
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

