---
title: Propriété canonique PidTagConversationIndex
description: Décrit la propriété canonique PidTagConversationIndex, qui contient une valeur binaire qui indique la position de ce message dans un thread de conversation.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
ms.openlocfilehash: 0ae56bbbd80acc6e8431d6d7b14968b9710b1021
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770991"
---
# <a name="pidtagconversationindex-canonical-property"></a>Propriété canonique PidTagConversationIndex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur binaire qui indique la position relative de ce message dans un thread de conversation. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Identificateur :  <br/> |0x0071  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Un thread de conversation représente une série de messages et de réponses. Cette propriété est généralement implémentée à l’aide de valeurs d’horodatage concaténées. Son utilisation est facultative, même si **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) est défini. 
  
MAPI fournit la fonction [ScCreateConversationIndex](sccreateconversationindex.md) pour créer ou mettre à jour un index de conversation. La fonction prend la valeur d’index actuelle en tant que tableau d’octets comptés et retourne la valeur d’index avec un horodatage concaténé à la fin. Un message représentant une réponse à un autre message doit utiliser **ScCreateConversationIndex** pour mettre à jour cette propriété. 
  
Un fournisseur de magasin de messages peut s’assurer que **PR_CONVERSATION_INDEX** est toujours défini sur les messages entrants ou sortants. Pour ce faire, il peut appeler **ScCreateConversationIndex**, soit avec la valeur existante si cette propriété est définie, soit avec NULL si ce n’est pas le cas. Cette action doit être effectuée avant [l’appel d’IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Tous les messages ayant la même valeur pour **PR_CONVERSATION_TOPIC** peuvent être triés sur cette propriété pour révéler la relation hiérarchique des messages. 
  
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

