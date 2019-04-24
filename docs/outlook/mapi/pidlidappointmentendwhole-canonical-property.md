---
title: Propriété canonique PidLidAppointmentEndWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358897"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a>Propriété canonique PidLidAppointmentEndWhole

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la date et l'heure de fin d'un rendez-vous.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptEndWhole  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Appointment  <br/> |
|ID long (couvercle):  <br/> |0x0000820E  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété correspond à la propriété **dispidApptEndWhole** du rendez-vous dans le modèle objet Microsoft Office Outlook. 
  
Cette énumération spécifie la date et l'heure de fin de l'événement; elle doit être au format UTC (temps universel coordonné) et doit être supérieure à la valeur de la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). Pour une série périodique, la propriété **dispidApptEndWhole** est la date et l'heure de fin de la première instance en fonction de la périodicité. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

