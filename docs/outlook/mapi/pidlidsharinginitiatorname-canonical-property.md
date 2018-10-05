---
title: Propriété canonique PidLidSharingInitiatorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorName
api_type:
- COM
ms.assetid: f2b126fc-41fa-4dc4-9f13-07bc4f621d0b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394378"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a>Propriété canonique PidLidSharingInitiatorName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Désigne comme une propriété d’un message de partage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingInitiatorName  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID de type long (capot) :  <br/> |0x00008A07  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie à la valeur de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à partir du carnet d’adresses identifié par **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) et doit être ignorée. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Partage des dossiers de boîte aux lettres entre des clients.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

