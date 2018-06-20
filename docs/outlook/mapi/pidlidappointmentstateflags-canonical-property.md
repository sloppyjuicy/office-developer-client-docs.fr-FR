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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785051"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a>Propriété canonique PidLidAppointmentStateFlags

  
  
**S’applique à**: Outlook 
  
Spécifie un champ de bits qui décrit l’état de l’objet.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptStateFlags  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008217  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est pas requise. Vous trouverez ci-dessous les indicateurs individuels qui peuvent être définies.
  
M (asfMeeting, 0 x 00000001)
  
> Cet indicateur indique que l’objet est un objet de la réunion ou d’un objet liées à la réunion.
    
R (asfReceived, 0 x 00000002)
  
> Cet indicateur indique que l’objet représenté a été reçu à partir d’une autre personne.
    
C (asfCanceled, 0 x 00000004)
  
> Cet indicateur indique que l’objet de la réunion représenté par l’objet a été annulée.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

