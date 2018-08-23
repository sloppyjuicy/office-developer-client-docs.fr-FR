---
title: Propriété canonique PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1ea252f8333bf39d391b8d99b768c9c3fa8e57ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568734"
---
# <a name="pidlidbusystatus-canonical-property"></a>Propriété canonique PidLidBusyStatus

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Représente la disponibilité de l’utilisateur pour un rendez-vous.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidBusyStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008205  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie la disponibilité d’un utilisateur pour l’événement décrit par l’objet et doit être une des valeurs ci-dessous.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |L'utilisateur est disponible.  <br/> |
|0x00000001  <br/> |L’utilisateur dispose d’un événement provisoire de prévu.  <br/> |
|0x00000002  <br/> |L'utilisateur est occupé.  <br/> |
|0 x 00000003  <br/> |L'utilisateur est absent du bureau.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
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

