---
title: Propriété canonique PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 03dcc9a1f929bc6f99ca9e1dd9f75f3fb9c3dcb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562966"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>Propriété canonique PidTagOriginalAuthorEntryId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|Identificateur :  <br/> |0x004C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une des propriétés d’adresse de l’auteur d’un message. Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Il n’est jamais modifié lorsque le message est transféré ou d’une réponse. 
  
Permet à la propriété author d’origine pour la conservation des informations à partir de l’extérieur du domaine de messagerie local. Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tels que depuis Internet, cette propriété fournit un moyen pour que les informations d’origine n’est pas perdue.
  
## <a name="related-resources"></a>Ressources connexes

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

