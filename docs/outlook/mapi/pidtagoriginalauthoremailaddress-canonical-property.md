---
title: Propriété canonique PidTagOriginalAuthorEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 670ebb8a50de98eaa9310bc3632cbb2b3e14e33e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599923"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a>Propriété canonique PidTagOriginalAuthorEmailAddress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’adresse e-mail de l’auteur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou d’y répondre.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x007A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse pour l’auteur d’un message. Lors de la première soumission du message, l’application cliente doit définir ces propriétés sur la valeur de la propriété **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)). Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue.
  
Les propriétés d’auteur d’origine permettent la conservation des informations en dehors du domaine de messagerie local. Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tel qu’Internet, ces propriétés permettent de s’assurer que les informations d’origine ne sont pas perdues.
  
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

