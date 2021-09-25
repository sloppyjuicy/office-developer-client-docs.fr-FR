---
title: Propriété canonique PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8b9b1b4615893418374b98403e7d519d3f632d07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591891"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>Propriété canonique PidLidAppointmentSubType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si l’événement s’agit de la journée.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptSubType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008215  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie si l’événement est un événement d’une journée, comme spécifié par l’utilisateur. La valeur TRUE indique que l’événement est un événement d’une journée, auquel cas l’heure de début et l’heure de fin doivent être minuit afin que la durée soit un multiple de 24 heures et d’au moins 24 heures. La valeur FALSE ou l’absence de cette propriété indique que l’événement n’est pas un événement d’une journée complète. Le client ou le serveur ne doit pas déduire la valeur comme TRUE lorsqu’un utilisateur crée un événement de 24 heures, même si l’événement commence et se termine à minuit.
  
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

