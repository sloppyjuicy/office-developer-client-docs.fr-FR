---
title: Propriété canonique PidTagDefaultStore
description: Décrit la propriété canonique PidTagDefaultStore, qui contient TRUE si un magasin de messages est le magasin de messages par défaut dans la table du magasin de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
ms.openlocfilehash: dc8b716152fa4b83e576edba90e1058954263aa8
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769542"
---
# <a name="pidtagdefaultstore-canonical-property"></a>Propriété canonique PidTagDefaultStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un magasin de messages est le magasin de messages par défaut dans la table du magasin de messages. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFAULT_STORE  <br/> |
|Identificateur :  <br/> |0x3400  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Magasin de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété apparaît sous la forme d’une colonne dans la table du magasin de messages. La valeur est basée sur **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
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

