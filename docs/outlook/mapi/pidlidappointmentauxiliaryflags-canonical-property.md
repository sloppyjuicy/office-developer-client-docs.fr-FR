---
title: Propriété canonique PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5e05144beeac8318b8c28153461742a491698996
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576626"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Propriété canonique PidLidAppointmentAuxiliaryFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie un champ de bits qui décrit l’état de l’objet auxiliaire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptAuxFlags  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008207  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est pas requise. Vous trouverez ci-dessous les indicateurs individuels qui peuvent être définies.
  
C (auxApptFlagCopied, 0 x 00000001)
  
> Cet indicateur indique que l’objet calendar a été copié à partir d’un autre dossier de calendrier.
    
R (auxApptFlagForceMtgResponse, 0 x 00000002)
  
> Cet indicateur sur une demande de réunion indique que le client ou le serveur doit envoyer une réponse à une réunion à l’organisateur lorsqu’une réponse est choisie.
    
F (auxApptFlagForwarded, 0 x 00000004)
  
> Cet indicateur sur une demande de réunion indique qu’il a été transféré (y compris transmis par l’organisateur), au lieu d’en cours d’une invitation à partir de l’organisateur.
    
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

