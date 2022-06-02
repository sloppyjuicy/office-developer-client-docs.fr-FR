---
title: Propriété canonique PidLidAppointmentRecur
description: La propriété canonique PidLidAppointmentRecur spécifie les dates et heures auxquelles une série périodique se produit à l’aide de l’un des modèles et plages de périodicité.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
ms.openlocfilehash: 2cf4460c7b46627edeaa6ecc027b969807902c51
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852291"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propriété canonique PidLidAppointmentRecur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les dates et heures auxquelles une série périodique se produit à l’aide de l’un des modèles et plages de périodicité spécifiés dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptRecur  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008216  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie les dates et heures auxquelles une série périodique se produit à l’aide de l’un des modèles et plages de périodicité détaillés dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). La valeur de cette propriété contient également des informations sur les exceptions modifiées et supprimées ; informations telles que les dates, l’objet, l’emplacement et plusieurs autres propriétés des exceptions. Les données binaires de cette propriété pour les éléments de calendrier périodiques sont stockées en tant que structure **AppointmentRecurrencePattern** . Cette propriété ne doit pas exister sur les éléments de calendrier d’instance unique. 
  
Il existe certaines limitations aux périodicités :
  
- Plusieurs instances ne doivent pas démarrer le même jour.
    
- Les occurrences ne doivent pas se chevaucher. Plus précisément, une exception qui modifie la date de début d’une instance de la série périodique doit se produire à une date postérieure à la fin de l’instance précédente et au début de l’instance suivante dans la série périodique. Il en va de même si les instances précédentes ou suivantes de la série périodique sont des exceptions.
    
La planification d’une série périodique est déterminée par son modèle de périodicité et sa plage.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour les rappels d’e-mail et d’autres objets.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

