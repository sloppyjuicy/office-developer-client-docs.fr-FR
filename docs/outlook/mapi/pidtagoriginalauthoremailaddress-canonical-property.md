---
title: Propriété canonique PidTagOriginalAuthorEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1954e1760fead9cbe13f0f2394f8095cab7f26ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786304"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a>Propriété canonique PidTagOriginalAuthorEmailAddress

  
  
**S’applique à**: Outlook 
  
Contient l’adresse de messagerie de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x007A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse de l’auteur d’un message. Au premier envoi du message, l’application cliente doit définir ces propriétés à la valeur de la propriété **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)). Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.
  
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

