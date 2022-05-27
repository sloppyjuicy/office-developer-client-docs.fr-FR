---
title: Propriété canonique PidTagOriginalAuthorSearchKey
description: Décrit la propriété canonique PidTagOriginalAuthorSearchKey, qui contient la clé de recherche de l’auteur de la première version d’un message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
ms.openlocfilehash: fd48eb511638ded50694516707411808f1a1e36d
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752532"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>Propriété canonique PidTagOriginalAuthorSearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la clé de recherche de l’auteur de la première version d’un message, c’est-à-dire le message avant d’être transféré ou auquel il a répondu.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x0056  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est l’une des propriétés d’adresse de l’auteur d’un message. Lors de la première soumission du message, l’application cliente doit définir cette propriété sur la valeur de la **PR_SENDER_SEARCH_KEY** propriété [PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md). Elle n’est jamais modifiée lorsque le message est transféré ou auquel il est répondu. 
  
Les propriétés de l’auteur d’origine permettent la conservation des informations provenant de l’extérieur du domaine de messagerie local. Lorsqu’un message arrive d’un autre domaine de messagerie, tel qu’Internet, ces propriétés permettent de s’assurer que les informations d’origine ne sont pas perdues.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

