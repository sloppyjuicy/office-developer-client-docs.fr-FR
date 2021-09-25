---
title: Propriété canonique PidTagDefaultStore
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4198b6f244c09045225bdd5e8392241edc9a45d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563685"
---
# <a name="pidtagdefaultstore-canonical-property"></a>Propriété canonique PidTagDefaultStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si une magasin de messages est la magasin de messages par défaut dans la table de la boutique de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEFAULT_STORE  <br/> |
|Identificateur :  <br/> |0x3400  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Magasin de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété apparaît en tant que colonne dans la table de la boutique de messages. La valeur est basée sur **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
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

