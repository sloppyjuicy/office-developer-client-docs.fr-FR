---
title: Propriété canonique PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334684"
---
# <a name="pidtagconversationtopic-canonical-property"></a>Propriété canonique PidTagConversationTopic

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le sujet du premier message dans un thread de conversation. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Identificateur :  <br/> |0x0070  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Un thread de conversation représente une série de messages et de réponses. Ces propriétés sont définies pour le premier message dans un thread, généralement pour la propriété **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). Les messages suivants dans le thread doivent utiliser la même rubrique sans modification. 
  
La propriété **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indique la relation de commande entre les messages et les réponses suivants. Son utilisation est facultative, même si ces propriétés sont définies. 
  
Un fournisseur de banque de messages a la possibilité de s'assurer que ces propriétés sont toujours définies sur les messages entrants ou sortants. Si ces propriétés sont déjà définies, elles ne doivent pas être modifiées. Si ce n'est pas le cas, ils peuvent être définis sur **PR_NORMALIZED_SUBJECT**. N'importe quelle action doit être effectuée avant l'appel de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

