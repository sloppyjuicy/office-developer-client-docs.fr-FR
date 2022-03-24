---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: Contient un flux qui m’indique le format persistant d’une structure TZDEFINITION, qui stocke la description du fuseau horaire utilisé.
ms.openlocfilehash: 06d070e6f941921cb23de7a86a68fa6d9bbd2dc9
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762689"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui ma visite le format persistant d’une structure [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description du fuseau horaire utilisé lors de la sélection de l’heure de fin d’un rendez-vous à instance unique ou d’une demande de réunion. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x0000825F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003 ou version antérieure et les solutions basées sur Collaboration Data Objects (CDO) 1.2.1 et qui n’ont pas exécuté l’outil de mise à jour du calendrier pour Outlook ou Microsoft Exchange Server, stockent l’heure de début et l’heure de fin des rendez-vous à instance unique et des demandes de réunion en temps universel coordonné (UTC). Ces clients ne stockent aucune information pour le fuseau horaire où le rendez-vous ou la demande de réunion est créé.
  
Les versions de Microsoft Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 qui exécutent l’outil de mise à jour du calendrier Outlook ou Exchange Server utilisent **dispidApptTZDefEndDisplay** pour stocker le fuseau horaire pour l’heure de fin. **dispidApptTZDefEndDisplay** affiche le rendez-vous ou la réunion dans le fuseau horaire d’origine qu’il a été programmé et détermine si l’heure de fin doit être ajustée si les règles du fuseau horaire changent. Si cette propriété est manquante, le fuseau horaire spécifié par la propriété **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) est utilisé. Si **dispidApptTZDefStartDisplay** est manquant ou non valide, le fuseau horaire local actuel est supposé. **dispidApptTZDefEndDisplay** est utilisé uniquement à des fins d’affichage et n’est pas utilisé dans l’extension de la récurrence. 
  
Un parseur doit être prudent lorsqu’il lit un flux obtenu à partir de **dispidApptTZDefEndDisplay**, ou lorsqu’il persiste **TZDEFINITION** dans un flux pour l’engagement envers une propriété binaire telle que **dispidApptTZDefEndDisplay**. Pour plus d’informations, [voir À propos de la persistance de TZDEFINITION dans un flux à valider dans une propriété binaire](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** spécifie les informations de fuseau horaire pour la propriété **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). Le format, les contraintes et le calcul de **dispidApptTZDefEndDisplay** sont les mêmes que spécifiés dans la propriété **dispidApptTZDefStartDisplay** . 
  
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

