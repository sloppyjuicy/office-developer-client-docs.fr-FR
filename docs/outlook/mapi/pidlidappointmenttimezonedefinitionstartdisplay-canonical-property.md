---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6e8bf65c960b40a43d13ae5253daa7f8cda69121
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782299"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui ma visite le format persistant d’une structure [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description du fuseau horaire utilisé lors de la sélection de l’heure de début d’un rendez-vous à instance unique ou d’une demande de réunion. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x0000825E  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003 ou version antérieure et les solutions basées sur Collaboration Data Objects (CDO) 1.2.1 et qui n’ont pas exécuté l’outil de mise à jour du calendrier pour Outlook ou Microsoft Exchange Server, stockent l’heure de début et l’heure de fin des rendez-vous à instance unique et des demandes de réunion en temps universel coordonné (UTC). Ces clients ne stockent aucune information pour le fuseau horaire dans lequel le rendez-vous ou la demande de réunion est créé.
  
Les versions de Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 qui exécutent l’outil de mise à jour du calendrier Outlook ou Exchange Server utilisent cette propriété pour stocker le fuseau horaire de l’heure de début. La **propriété dispidApptTZDefStartDisplay** affiche le rendez-vous ou la réunion dans le fuseau horaire d’origine qui a été programmé. Il détermine si l’heure de début doit être ajustée si les règles du fuseau horaire changent. Si cette propriété est manquante, le fuseau horaire local actuel est supposé. Cette propriété est utilisée uniquement à des fins d’affichage et n’est pas utilisée dans l’extension de la récurrence. 
  
Un robot doit être prudent lorsqu’il lit un flux obtenu à partir de cette propriété, ou lorsqu’il fait persister **TZDEFINITION** dans un flux pour s’engager auprès d’une propriété binaire telle que **dispidApptTZDefStartDisplay**. Pour plus d’informations, [voir À propos de la persistance de TZDEFINITION dans un flux à valider dans une propriété binaire](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Cette propriété spécifie les informations de fuseau horaire pour la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). La valeur de **dispidApptTZDefStartDisplay** est utilisée pour convertir la date et l’heure de début de l’heure UTC au fuseau horaire local à des fins d’affichage. Pour chaque **TZRULE** spécifié par cette propriété, l’TZRULE_FLAG_RECUR_CURRENT_TZREG ne doit pas être définie. Par exemple, si **TZRULE** est la règle effective, la valeur du champ, **TZRULE** doit être « 0x0002 » ; Dans le cas contraire, il doit s'0x0000. 
  
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

