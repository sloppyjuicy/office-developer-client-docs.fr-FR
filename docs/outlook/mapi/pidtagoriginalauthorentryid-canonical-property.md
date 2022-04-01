---
title: Propriété canonique PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: Contient l’identificateur d’entrée de l’auteur de la première version d’un message, qui est le message avant d’être transmis ou auquel il a été répondu.
ms.openlocfilehash: 65c5d3bf91ce1ab63ab3dfdbea459c246f8b3d2a
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523294"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>Propriété canonique PidTagOriginalAuthorEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de l’auteur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou de répondre.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|Identificateur :  <br/> |0x004C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est l’une des propriétés d’adresse de l’auteur d’un message. Lors de la première soumission du message, l’application cliente doit définir cette propriété sur la valeur **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue. 
  
La propriété d’auteur d’origine permet la conservation des informations en dehors du domaine de messagerie local. Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tel qu’Internet, cette propriété permet de s’assurer que les informations d’origine ne sont pas perdues.
  
## <a name="related-resources"></a>Ressources connexes

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

