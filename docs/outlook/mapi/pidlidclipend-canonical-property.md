---
title: Propriété canonique PidLidClipEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386067"
---
# <a name="pidlidclipend-canonical-property"></a>Propriété canonique PidLidClipEnd

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la date de fin et l’heure de l’événement dans le temps universel coordonné (UTC) pour les objets de calendrier d’instance unique. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidClipEnd  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008236  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Pour les objets de calendrier d’instance unique, il spécifie la date de fin et l’heure de l’événement au format UTC. Pour une série périodique, cette propriété spécifie minuit à la date de la dernière instance de la série périodique au format UTC, sauf si la série périodique n’a aucun effet, auquel cas la valeur doit être le 31 août 4500, 11:59 p.m.
  
La valeur de cette propriété doit être définie à la valeur de la **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

