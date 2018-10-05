---
title: Propriété canonique PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393368"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propriété canonique PidLidAppointmentRecur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les dates et heures quand une série périodique se produit à l’aide d’une des plages qui sont spécifiés dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)les périodicités.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptRecur  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008216  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie les dates et heures quand une série périodique se produit à l’aide d’un des modèles de périodicité et des plages détaillé dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). La valeur de cette propriété contient également des informations sur les exceptions modifiées et supprimées ; informations telles que les dates, objet, emplacement et plusieurs autres propriétés des exceptions. Les données binaires dans cette propriété pour les éléments de calendrier périodiques sont stockées en tant que la structure **AppointmentRecurrencePattern** . Cette propriété ne doit pas exister sur les éléments de calendrier d’instance unique. 
  
Il existe certaines limitations pour les périodicités :
  
- Plusieurs instances ne doivent pas commencer le même jour.
    
- Occurrences ne doivent pas se chevaucher. Plus précisément, une exception qui modifie la date de début d’une instance de la série périodique doit se produire sur une date postérieure à la fin de l’instance précédente et le début de l’occurrence suivante de la série périodique. Les mêmes a la valeur true si les instances précédents ou suivant dans la série périodique sont les exceptions.
    
La planification d’une série périodique est déterminée par sa périodicité et la plage.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

