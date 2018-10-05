---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382749"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Propriété canonique PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui mappe sur le format persistant d’une structure [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description pour le fuseau horaire qui est utilisé lorsque l’heure de fin d’un rendez-vous ou d’une demande de réunion est sélectionné. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x0000825F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003 ou version antérieure et les solutions qui sont basées sur les objets CDO (Collaboration Data) 1.2.1 et qui n’ont pas exécuter l’outil de mise à jour de calendrier pour Outlook ou Microsoft Exchange Server, stockent l’heure de début et heure de fin de l’instance unique rendez-vous et demandes de réunion en temps universel coordonné (UTC). Ces clients ne stockent pas les informations pour le fuseau horaire dans lequel la demande de réunion ou de rendez-vous est créée.
  
Mettre à jour les versions de Microsoft Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 qui ont été exécutés le calendrier Outlook ou Exchange Server outil utiliser **dispidApptTZDefEndDisplay** pour stocker le fuseau horaire de l’heure de fin. **dispidApptTZDefEndDisplay** affiche le rendez-vous ou la réunion dans le fuseau horaire d’origine qu’elle a été planifiée et détermine si l’heure de fin doit être ajustée si Modifier les règles du fuseau horaire. Si cette propriété est manquante, le fuseau horaire spécifié par la propriété **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) est utilisé. Si **dispidApptTZDefStartDisplay** est manquant ou non valide, le fuseau horaire local est supposé. **dispidApptTZDefEndDisplay** est utilisé à des fins d’affichage uniquement et n’est pas utilisée dans l’extension de périodicité. 
  
Un analyseur doit être prudent lorsqu’il lit un flux de données provenant de **dispidApptTZDefEndDisplay**, ou lorsqu’il persiste **TZDEFINITION** à un flux d’engagement à une propriété binaire, tel que **dispidApptTZDefEndDisplay**. Pour plus d’informations, voir [About persistance TZDEFINITION dans un flux de validation dans une propriété binaire](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** spécifie les informations de fuseau horaire pour la propriété **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). Le format, les contraintes et calcul de **dispidApptTZDefEndDisplay** sont les mêmes que spécifié dans la propriété **dispidApptTZDefStartDisplay** . 
  
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

