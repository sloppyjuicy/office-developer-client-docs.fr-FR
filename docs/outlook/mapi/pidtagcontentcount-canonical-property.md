---
title: Propriété canonique PidTagContentCount
description: Décrit la propriété canonique PidTagContentCount, qui contient le nombre de messages dans un dossier, tel qu’il est calculé par le magasin de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
ms.openlocfilehash: 49954ff53bc9c95022e00675d36e501d4ad63539
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770109"
---
# <a name="pidtagcontentcount-canonical-property"></a>Propriété canonique PidTagContentCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nombre de messages dans un dossier, tel qu’il est calculé par le magasin de messages.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_COUNT  <br/> |
|Identificateur :  <br/> |0x3602  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété calculée par le magasin de messages est utilisée à deux fins différentes, bien que liées. Sur un objet MapiFolder, il contient le nombre de messages dans un dossier. Dans une ligne de titre dans des tables MAPI classées, elle contient le nombre de messages non associés dans la catégorie correspondant à cette ligne de titre.
  
Le nombre contenu dans cette propriété n’inclut pas les entrées associées dans le dossier. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contient le nombre de messages non lus pour le dossier. Une application cliente peut lire cette propriété et **PR_CONTENT_UNREAD**, mais pas la modifier. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Microsoft Exchange Server associées.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de table de base.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

