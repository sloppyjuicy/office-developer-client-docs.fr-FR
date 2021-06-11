---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345352"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionRecur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui ma visite le format persistant d’une structure [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) qui stocke la description du fuseau horaire utilisé lors de la création d’un rendez-vous périodique ou d’une demande de réunion. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefRecur  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008260  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Les versions de Microsoft Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO (Collaboration Data Objects) 1.2.1 qui exécutent l’outil de mise à jour du calendrier Outlook ou Exchange Server utilisent les propriétés **dispidApptTZDefRecur** et **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) pour déterminer si la réunion périodique doit être ajustée si les règles du fuseau horaire changent. Ces propriétés doivent être synchronisées, car les clients plus anciens peuvent toujours manipuler la **propriété dispidTimeZoneStruct.** Pour détecter si les deux propriétés sont synchronisées, le membre **wFlags** de la règle qui correspond à **dispidTimeZoneStruct** doit avoir l’indicateur TZRULE_FLAG_RECUR_CURRENT_TZREG définie. Si cet indicateur n’est pas définie ou si elle est définie et que la règle dans la propriété **dispidTimeZoneStruct** ne correspond pas à la règle marquée, la propriété **dispidApptTZDefRecur** doit être ignorée et **dispidTimeZoneStruct** doit être utilisée à la place. 
  
Lorsque vous écrivez les propriétés **dispidApptTZDefRecur** et **dispidTimeZoneStruct** dans une nouvelle réunion périodique, ou lorsque vous faites un choix arbitraire d’utiliser la propriété **dispidTimeZoneStruct,** la définition actuelle du fuseau horaire (conformément au Registre Windows) doit être utilisée. 
  
Un parseur doit être prudent lorsqu’il lit un flux qui est obtenu à partir de **dispidApptTZDefRecur**, ou lorsqu’il persiste **TZDEFINITION** dans un flux pour l’engagement envers une propriété binaire telle que **dispidApptTZDefRecur**. Pour plus d’informations, voir [À propos de la persistance de TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)dans un flux à valider dans une propriété binaire.
  
 **dispidApptTZDefRecur** spécifie les informations de fuseau horaire qui décrivent comment convertir la date et l’heure de la réunion d’une série périodique vers et à partir du temps universel coordonné (UTC). Si cette propriété est définie mais qu’elle a des données incohérentes avec les données représentées par **dispidTimeZoneStruct**, le client doit utiliser **dispidTimeZoneStruct** au lieu de **dispidApptTZDefRecur**. Si **dispidApptTZDefRecur** n’est pas définie, la propriété **PidLidTimeZoneStruct** sera utilisée à la place. Les champs de cet objet BLOB sont codés dans un ordre d’byte peu endian. 
  
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

