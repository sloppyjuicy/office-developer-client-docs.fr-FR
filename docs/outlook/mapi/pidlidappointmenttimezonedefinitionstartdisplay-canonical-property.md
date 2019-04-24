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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345016"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui correspond au format persistant d'une structure [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description du fuseau horaire utilisé lorsque l'heure de début d'une demande de réunion ou de rendez-vous à instance unique est sélectionnée. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Appointment  <br/> |
|ID long (couvercle):  <br/> |0x0000825E  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003 ou une version antérieure, ainsi que les solutions basées sur CDO (Collaboration Data Objects) 1.2.1 et qui n'ont pas exécuté l'outil de mise à jour de calendrier pour Outlook ou Microsoft Exchange Server, stockent l'heure de début et l'heure de fin d'une instance unique rendez-vous et demandes de réunion au format UTC (Coordinated Universal Time). Ces clients ne stockent aucune information pour le fuseau horaire dans lequel la demande de rendez-vous ou de réunion est créée.
  
Les versions d'Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 qui exécutent l'outil de mise à jour de calendrier Outlook ou Exchange Server utilisent cette propriété pour stocker le fuseau horaire pour l'heure de début. La propriété **dispidApptTZDefStartDisplay** indique le rendez-vous ou la réunion dans le fuseau horaire d'origine qu'il était planifié. Il détermine si l'heure de début doit être ajustée si les règles du fuseau horaire changent. Si cette propriété est manquante, le fuseau horaire local actuel est utilisé. Cette propriété est utilisée à des fins d'affichage uniquement et n'est pas utilisée dans le développement de périodicité. 
  
Un analyseur doit être prudent lorsqu'il lit un flux obtenu à partir de cette propriété, ou lorsqu'il rend **TZDEFINITION** à un flux pour engagement à une propriété binaire telle que **dispidApptTZDefStartDisplay**. Pour plus d'informations, consultez la rubrique [about persistING TZDEFINITION to a Stream to commit to a Binary Property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Cette propriété spécifie les informations de fuseau horaire pour la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). La valeur de **dispidApptTZDefStartDisplay** est utilisée pour convertir la date et l'heure de début à partir de l'UTC vers le fuseau horaire local à des fins d'affichage. Pour chaque **TZRULE** spécifié par cette propriété, l'indicateur TZRULE_FLAG_RECUR_CURRENT_TZREG ne doit pas être défini. Par exemple, si **TZRULE** est la règle effective, la valeur du champ, **TZRULE** doit être «0x0002»; Sinon, il doit s'agir de «0x0000». 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées..
    
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

