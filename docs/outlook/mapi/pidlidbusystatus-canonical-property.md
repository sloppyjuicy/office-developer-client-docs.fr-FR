---
title: PidLidBusyStatus, propriété canonique
description: Décrit la propriété canonique PidLidBusyStatus, qui représente la disponibilité de l’utilisateur pour un rendez-vous.
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
ms.openlocfilehash: 5aa973435e53f81f1e06eebbbd3a0673d0f80357
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852942"
---
# <a name="pidlidbusystatus-canonical-property"></a>PidLidBusyStatus, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la disponibilité de l’utilisateur pour un rendez-vous.
  
|Propriété |Valeur |
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
|0x00000000  <br/> |L'utilisateur est disponible. |
|0x00000001  <br/> |Un événement provisoire est planifié pour l’utilisateur. |
|0x00000002  <br/> |L'utilisateur est occupé. |
|0x00000003  <br/> |L'utilisateur est absent du bureau. |
   
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

