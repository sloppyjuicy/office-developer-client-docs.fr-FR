---
title: Propriété canonique PidLidClipEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: Spécifie la date et l’heure de fin de l’événement en temps universel coordonné (UTC) pour les objets calendrier d’instance unique.
ms.openlocfilehash: 09fef151b63e8809bcba98ca947d58554b1dbf61
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762367"
---
# <a name="pidlidclipend-canonical-property"></a>Propriété canonique PidLidClipEnd

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la date et l’heure de fin de l’événement en temps universel coordonné (UTC) pour les objets calendrier d’instance unique. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidClipEnd  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008236  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Pour les objets de calendrier d’instance unique, il spécifie la date et l’heure de fin de l’événement au UTC. Pour une série périodique, cette propriété spécifie minuit à la date de la dernière instance de la série périodique au UTC, sauf si la série périodique n’a pas de fin, auquel cas la valeur doit être 31 août 4500, 23:59.
  
La valeur de cette propriété doit être définie sur la valeur du **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

