---
title: Propriété canonique PidLidSharingLocalType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSharingLocalType
api_type:
- COM
ms.assetid: 6ac438a1-d36f-424f-b4b4-d6f2d26fd350
description: Spécifie la valeur de la propriété PR_CONTAINER_CLASS du dossier partagé. Il s’agit d’une propriété d’un message de partage.
ms.openlocfilehash: 73314c3e760e166444887474295272d82c06960f
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405915"
---
# <a name="pidlidsharinglocaltype-canonical-property"></a>Propriété canonique PidLidSharingLocalType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la valeur de la propriété **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) du dossier partagé. Il s’agit d’une propriété d’un message de partage.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingLocalType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID long (LID) :  <br/> |0x00008A14  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être l’une des suivantes :
  
- « IPF. Rendez-vous »
    
- « IPF. Contact »
    
- « IPF. Tâche »
    
- « IPF. StickyNote »
    
- « IPF. Journal »
    
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

