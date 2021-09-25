---
title: Propri t canonique PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b0e0b20023d3ce18d6ffbc5363d15cd6e2a619d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563993"
---
# <a name="pidlidbusystatus-canonical-property"></a>Propri t canonique PidLidBusyStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la disponibilité de l’utilisateur pour un rendez-vous.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidBusyStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008205  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie la disponibilité d’un utilisateur pour l’événement décrit par l’objet et doit être l’une des valeurs spécifiées ci-dessous.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |L'utilisateur est disponible.  <br/> |
|0x00000001  <br/> |Un événement provisoire est prévu pour l’utilisateur.  <br/> |
|0x00000002  <br/> |L'utilisateur est occupé.  <br/> |
|0x00000003  <br/> |L'utilisateur est absent du bureau.  <br/> |
   
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

