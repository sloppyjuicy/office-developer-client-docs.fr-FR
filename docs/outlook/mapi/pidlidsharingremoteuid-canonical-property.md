---
title: Propriété canonique PidLidSharingRemoteUid
description: Décrit la propriété canonique PidLidSharingRemoteUid, qui spécifie l’ID d’entrée du dossier distant partagé.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
ms.openlocfilehash: cf8b3f60a4534916b57f72ca94dfc70186f68bd5
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816086"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a>Propriété canonique PidLidSharingRemoteUid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’ID d’entrée du dossier distant partagé. Il s’agit d’une propriété d’un message de partage.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingRemoteUid  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID long (LID) :  <br/> |0x00008A06  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur la représentation de chaîne hexadécimale de la valeur de la propriété PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) sur le dossier partagé. Il s’agit d’une propriété d’un message de partage.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Partage des dossiers de boîte aux lettres entre les clients.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

