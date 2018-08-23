---
title: Propriété canonique PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b489e73f9453e5d2ae6657969c2bc18fc9a4620e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562938"
---
# <a name="pidtagcontentcount-canonical-property"></a>Propriété canonique PidTagContentCount

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le nombre de messages dans un dossier, calculé par la banque de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_COUNT  <br/> |
|Identificateur :  <br/> |0x3602  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété calculée par la banque de messages est utilisée pour les deux, même si associées, à des fins. Dans un objet MapiFolder, il contient le nombre de messages dans un dossier. Dans une ligne d’en-tête dans les tableaux MAPI par catégorie, il contient le nombre de messages non associés dans les catégories correspondant à cette ligne d’en-tête.
  
Nombre figurant dans cette propriété n’inclut pas les entrées associées dans le dossier. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contient le nombre de messages non lus du dossier. Une application cliente peut lire mais pas modifier cette propriété et la **PR_CONTENT_UNREAD**. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de la table principale.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

