---
title: Propriété canonique PidTagObsoletedMessageIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagObsoletedMessageIds
api_type:
- HeaderDef
ms.assetid: bc979398-f1ad-4496-b982-428b95719369
description: Contient les identificateurs des messages que ce message a la place. Les identificateurs sont des clés de recherche standard utilisant le format de PR_SEARCH_KEY propriété.
ms.openlocfilehash: 0fc594cbba41d9eb308ef662a45533b7d0466676
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524056"
---
# <a name="pidtagobsoletedmessageids-canonical-property"></a>Propriété canonique PidTagObsoletedMessageIds

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les identificateurs des messages que ce message a la place.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_OBSOLETED_IPMS  <br/> |
|Identificateur :  <br/> |0x001F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Les identificateurs contenus dans cette propriété sont des clés de recherche standard utilisant le format de la **propriété PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

