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
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329238"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a>Propriété canonique PidTagOriginalAuthorEmailAddress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'adresse de messagerie de l'auteur de la première version d'un message, c'est-à-dire le message avant son transfert ou sa réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x007A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d'adresse pour l'auteur d'un message. Lors de la première soumission du message, l'application cliente doit définir ces propriétés sur la valeur de la propriété **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)). Il n'est jamais modifié lorsque le message est transféré ou renvoyé.
  
Les propriétés de l'auteur d'origine permettent la conservation des informations en dehors du domaine de messagerie local. Lorsqu'un message arrive à partir d'un autre domaine de messagerie, tel qu'Internet, ces propriétés permettent de s'assurer que les informations d'origine ne sont pas perdues.
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

