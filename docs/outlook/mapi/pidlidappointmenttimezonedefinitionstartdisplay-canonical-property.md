---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay
description: Décrit la propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay, qui contient un flux qui correspond au format persistant d’une structure.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
ms.openlocfilehash: 5f76d8eb1f9ab50776706fe4d49ba394f77617de
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893717"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui correspond au format persistant d’une structure [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description du fuseau horaire utilisé lorsque l’heure de début d’un rendez-vous ou d’une demande de réunion à instance unique est sélectionnée. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x0000825E  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003 ou version antérieure, et les solutions basées sur Collaboration Data Objects (CDO) 1.2.1 et qui n’ont pas exécuté l’outil de mise à jour du calendrier pour Outlook ou Microsoft Exchange Server, stockent l’heure de début et l’heure de fin des rendez-vous à instance unique et des demandes de réunion en temps universel coordonné (UTC). Ces clients ne stockent aucune information pour le fuseau horaire dans lequel la demande de rendez-vous ou de réunion est créée.
  
Les versions d’Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 qui ont exécuté l’outil de mise à jour du calendrier Outlook ou Exchange Server utilisent cette propriété pour stocker le fuseau horaire de l’heure de début. La propriété **dispidApptTZDefStartDisplay** affiche le rendez-vous ou la réunion dans le fuseau horaire d’origine planifié. Il détermine si l’heure de début doit être ajustée si les règles du fuseau horaire changent. Si cette propriété est manquante, le fuseau horaire local actuel est supposé. Cette propriété est utilisée à des fins d’affichage uniquement et n’est pas utilisée dans l’extension de périodicité. 
  
Un analyseur doit être prudent lorsqu’il lit un flux obtenu à partir de cette propriété ou lorsqu’il conserve **TZDEFINITION** dans un flux pour l’engagement à une propriété binaire telle que **dispidApptTZDefStartDisplay**. Pour plus d’informations, consultez [À propos de la persistance de TZDEFINITION dans un flux pour valider une propriété binaire](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Cette propriété spécifie des informations de fuseau horaire pour la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). La valeur de **dispidApptTZDefStartDisplay** est utilisée pour convertir la date et l’heure de début de l’heure UTC en fuseau horaire local à des fins d’affichage. Pour chaque **TZRULE** spécifié par cette propriété, l’indicateur TZRULE_FLAG_RECUR_CURRENT_TZREG ne doit pas être défini. Par exemple, si **TZRULE** est la règle effective, la valeur du champ, **TZRULE** doit être « 0x0002 » ; sinon, il doit être « 0x0000 ». 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

