---
title: Propriété canonique PidLidAppointmentStateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345359"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a>Propriété canonique PidLidAppointmentStateFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un champ de bits qui décrit l’état de l’objet.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptStateFlags  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008217  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est pas obligatoire. Vous trouverez ci-dessous les indicateurs individuels qui peuvent être définies.
  
M (asfMeeting, 0x00000001)
  
> Cet indicateur indique que l’objet est un objet de réunion ou un objet lié à la réunion.
    
R (asfReceived, 0x00000002)
  
> Cet indicateur indique que l’objet représenté a été reçu d’une autre personne.
    
C (asfCanceled, 0x00000004)
  
> Cet indicateur indique que l’objet réunion représenté par l’objet a été annulé.
    
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

