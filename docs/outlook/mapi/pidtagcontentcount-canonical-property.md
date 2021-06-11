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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331954"
---
# <a name="pidtagcontentcount-canonical-property"></a>Propriété canonique PidTagContentCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nombre de messages dans un dossier, tel que calculé par la boutique de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_COUNT  <br/> |
|Identificateur :  <br/> |0x3602  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Dossier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété calculée par la boutique de messages est utilisée à deux fins différentes, bien qu’associées. Sur un objet MapiFolder, il contient le nombre de messages dans un dossier. Dans une ligne de titre dans les tableaux MAPI catégorisés, il contient le nombre de messages non associés dans la catégorie correspondant à cette ligne de titre.
  
Le numéro contenu dans cette propriété n’inclut pas les entrées associées dans le dossier. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contient le nombre de messages non lus pour le dossier. Une application cliente peut lire, mais pas modifier cette propriété et **PR_CONTENT_UNREAD**. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Microsoft Exchange Server protocole.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de table principale.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

