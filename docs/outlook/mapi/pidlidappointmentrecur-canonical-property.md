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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331779"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propriété canonique PidLidAppointmentRecur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les dates et heures auxquelles une série périodique se produit en utilisant l'une des plages et périodicités spécifiées dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptRecur  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Appointment  <br/> |
|ID long (couvercle):  <br/> |0x00008216  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie les dates et heures auxquelles une série périodique se produit à l'aide de l'une des périodicités et des plages détaillées dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). La valeur de cette propriété contient également des informations sur les exceptions modifiées et supprimées; informations telles que les dates, l'objet, l'emplacement et plusieurs autres propriétés d'exceptions. Les données binaires de cette propriété pour les éléments de calendrier périodiques sont stockées en tant que structure **AppointmentRecurrencePattern** . Cette propriété ne doit pas exister sur des éléments de calendrier d'instance unique. 
  
Il existe certaines limitations à la récurrence:
  
- Les instances multiples ne doivent pas commencer le même jour.
    
- Les occurrences ne doivent pas se chevaucher. Plus précisément, une exception qui modifie la date de début d'une instance dans la série périodique doit se produire à une date postérieure à la fin de l'instance précédente et au début de l'instance suivante dans la série périodique. Il en est de même si les instances précédente ou suivante de la série périodique sont des exceptions.
    
La planification d'une série périodique est déterminée par sa périodicité et sa plage.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d'interaction pour les rappels de messagerie et d'objet.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

