---
title: Propriété canonique PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e5b283376d018b7b2675e05f994d586126437590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786298"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>Propriété canonique PidTagOriginalAuthorSearchKey

  
  
**S’applique à**: Outlook 
  
Contient la clé de recherche de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x0056  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une des propriétés d’adresse de l’auteur d’un message. Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de la propriété[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_SEARCH_KEY**. Il n’est jamais modifié lorsque le message est transféré ou d’une réponse. 
  
Les propriétés de l’auteur d’origine autoriser pour la conservation des informations à partir de l’extérieur du domaine de messagerie local. Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tels qu’à partir d’Internet, ces propriétés fournissent un moyen pour vous assurer que les informations d’origine ne sont pas perdues.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

