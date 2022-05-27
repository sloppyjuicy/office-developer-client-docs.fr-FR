---
title: Propriété canonique PidTagRecipientProposedEndTime
description: Décrit la propriété canonique PidTagRecipientProposedEndTime, qui indique une heure de fin proposée d’une réunion.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
ms.openlocfilehash: 5b0b0dccffe91609c7d64e461a22f10292e1bf10
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752378"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a>Propriété canonique PidTagRecipientProposedEndTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique une heure de fin proposée d’une réunion.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_PROPOSEDENDTIME  <br/> |
|Identificateur :  <br/> |0x5FE4  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Destinataire du transport  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque la valeur de la propriété **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) est définie sur TRUE, la valeur de cette propriété indique la valeur demandée par le participant à définir comme valeur de la propriété **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) pour l’objet de réunion d’instance unique ou l’objet exception.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

