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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389301"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionRecur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui mappe sur le format persistant d’une structure [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description pour le fuseau horaire qui est utilisé lors de la création d’une demande de réunion ou un rendez-vous périodique. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefRecur  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008260  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Mettre à jour des versions de Microsoft Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur les objets CDO (Collaboration Data) 1.2.1 qui ont été exécutés le calendrier Outlook ou Exchange Server outil à utiliser le **dispidApptTZDefRecur** et ** dispidTimeZoneStruct** propriétés ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) pour déterminer si la réunion périodique doit être ajustée si Modifier les règles du fuseau horaire. Ces propriétés doivent être synchronisées, étant donné que les clients antérieurs peuvent toujours manipuler la propriété **dispidTimeZoneStruct** . Pour détecter si les deux propriétés sont synchronisées, le membre **wFlags** pour la règle qui correspond à **dispidTimeZoneStruct** doit être l’indicateur TZRULE_FLAG_RECUR_CURRENT_TZREG défini. Si cet indicateur n’est pas défini, ou elle est définie et la règle dans la propriété **dispidTimeZoneStruct** ne correspond pas à la règle marquée, la propriété **dispidApptTZDefRecur** doit être ignorée et **dispidTimeZoneStruct** doit être utilisé à la place. 
  
Lorsque vous écrivez les **dispidApptTZDefRecur** **dispidTimeZoneStruct** propriétés et à une nouvelle réunion périodique, ou, lorsque vous effectuez un choix arbitraire d’utiliser la propriété **dispidTimeZoneStruct** , la définition actuelle pour le fuseau horaire) en fonction du Registre Windows) doit être utilisé. 
  
Un analyseur doit être prudent lorsqu’il lit un flux qui est obtenu à partir de **dispidApptTZDefRecur**, ou lorsqu’il persiste **TZDEFINITION** à un flux d’engagement à une propriété binaire, tel que **dispidApptTZDefRecur**. Pour plus d’informations, voir [About persistance TZDEFINITION dans un flux de validation dans une propriété binaire](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** spécifie les informations de fuseau horaire qui explique comment convertir la date de la réunion et l’heure d’une série périodique vers et à partir du temps universel coordonné (UTC). Si cette propriété est définie, mais elle comporte des données ne sont pas cohérentes avec les données représentées par **dispidTimeZoneStruct**, le client doit utiliser **dispidTimeZoneStruct** au lieu de **dispidApptTZDefRecur**. Si **dispidApptTZDefRecur** n’est pas définie, la propriété **PidLidTimeZoneStruct** être utilisée à la place. Les champs de ce BLOB sont codés dans l’ordre de primauté des octets. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

