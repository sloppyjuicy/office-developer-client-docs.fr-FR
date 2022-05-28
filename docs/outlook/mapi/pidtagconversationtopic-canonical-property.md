---
title: Propriété canonique PidTagConversationTopic
description: Décrit la propriété canonique PidTagConversationTopic, qui contient la rubrique du premier message dans un thread de conversation.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
ms.openlocfilehash: 91989aab1854de0bbf70178bb453bc1c41bd3090
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770179"
---
# <a name="pidtagconversationtopic-canonical-property"></a>Propriété canonique PidTagConversationTopic

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la rubrique du premier message dans un thread de conversation. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Identificateur :  <br/> |0x0070  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Un thread de conversation représente une série de messages et de réponses. Ces propriétés sont définies pour le premier message d’un thread, généralement sur la propriété **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). Les messages suivants dans le thread doivent utiliser la même rubrique sans modification. 
  
La propriété **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indique la relation d’ordre entre les messages suivants et les réponses. Son utilisation est facultative, même si ces propriétés sont définies. 
  
Un fournisseur de magasin de messages peut s’assurer que ces propriétés sont toujours définies sur les messages entrants ou sortants. Si ces propriétés sont déjà définies, elles ne doivent pas être modifiées. Si ce n’est pas le cas, ils peuvent être définis sur **PR_NORMALIZED_SUBJECT**. Toute action doit être effectuée avant [l’appel d’IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées sur les objets de courrier électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

