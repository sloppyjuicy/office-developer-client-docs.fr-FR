---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6ca53633f0c1e5b226f7e03c8ee702d4cda7d115
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586794"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un flux qui mappe sur le format persistant d’une structure [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description pour le fuseau horaire qui est utilisé lorsque l’heure de début d’un rendez-vous ou d’une demande de réunion est sélectionné. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x0000825E  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003 ou version antérieure et les solutions qui sont basées sur les objets CDO (Collaboration Data) 1.2.1 et qui n’ont pas exécuter l’outil de mise à jour de calendrier pour Outlook ou Microsoft Exchange Server, stockent l’heure de début et heure de fin de l’instance unique rendez-vous et demandes de réunion en temps universel coordonné (UTC). Ces clients ne stockent pas les informations pour le fuseau horaire dans lequel la demande de réunion ou de rendez-vous est créée.
  
Versions d’Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 et que vous ont exécuté l’outil de mise à jour de calendrier Outlook ou Exchange Server, utilisent cette propriété pour stocker le fuseau horaire de l’heure de début. La propriété **dispidApptTZDefStartDisplay** indique le rendez-vous ou la réunion dans le fuseau horaire d’origine qu’il a été planifiée. Il détermine si l’heure de début doit être ajusté si Modifier les règles du fuseau horaire. Si cette propriété est manquante, le fuseau horaire local est supposé. Cette propriété est utilisée uniquement à des fins d’affichage et n’est pas utilisée dans l’extension de périodicité. 
  
Un analyseur doit être prudent lorsqu’il lit un flux de données obtenu à partir de cette propriété, ou lorsqu’il persiste **TZDEFINITION** à un flux d’engagement à une propriété binaire, tel que **dispidApptTZDefStartDisplay**. Pour plus d’informations, voir [About persistance TZDEFINITION dans un flux de validation dans une propriété binaire](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Cette propriété spécifie les informations de fuseau horaire pour la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). La valeur de **dispidApptTZDefStartDisplay** est utilisée pour convertir la date de début et l’heure UTC du fuseau horaire local à des fins d’affichage. Pour chaque **TZRULE** spécifié par cette propriété, l’indicateur TZRULE_FLAG_RECUR_CURRENT_TZREG ne doit pas être définie. Par exemple, si la **TZRULE** est la règle effective, la valeur du champ, **TZRULE** doit être « 0 x 0002 » ; dans le cas contraire, elle doit être « 0 x 0000 ». 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes...
    
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

