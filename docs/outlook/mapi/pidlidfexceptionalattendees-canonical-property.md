---
title: Propriété canonique PidLidFExceptionalAttendees
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2922b4864d07e53f2a51ae6ac298f1509bc66e01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620414"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a>Propriété canonique PidLidFExceptionalAttendees

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si cette propriété est un objet calendrier périodique avec une ou plusieurs exceptions, et qu’au moins l’une des exceptions incorporées a au moins un RecipientRow.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidFExceptionalAttendees  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x0000822B  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur FALSE ou l’absence de cette propriété indique que l’objet calendrier n’a pas d’exceptions ou qu’aucun des messages incorporés d’exception n’a RecipientRows.
  
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

