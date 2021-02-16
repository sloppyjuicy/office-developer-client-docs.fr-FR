---
title: Propriété canonique PidLidSharingInitiatorSmtp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eb699b2312064f8ed330238962dd86992c046139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337120"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a>Propriété canonique PidLidSharingInitiatorSmtp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’adresse SMTP de l’utilisateur qui a initié le message de partage. Il s’agit d’une propriété d’un message de partage. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingInitiatorSmtp  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID long (LID) :  <br/> |0x00008A08  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur la valeur de la propriété **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) à partir du carnet d’adresses identifié par la propriété **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) et doit être ignorée.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Partage des dossiers de boîte aux lettres entre clients.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

