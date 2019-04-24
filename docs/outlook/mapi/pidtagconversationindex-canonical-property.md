---
title: Propriété canonique PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334719"
---
# <a name="pidtagconversationindex-canonical-property"></a>Propriété canonique PidTagConversationIndex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur binaire qui indique la position relative de ce message dans un thread de conversation. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Identificateur :  <br/> |0x0071  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Un thread de conversation représente une série de messages et de réponses. Cette propriété est généralement implémentée à l'aide de valeurs de datage concaténées. Son utilisation est facultative, même si **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) est défini. 
  
MAPI fournit la fonction [ScCreateConversationIndex](sccreateconversationindex.md) pour créer ou mettre à jour un index de conversation. La fonction prend la valeur d'index actuelle en tant que tableau d'octets compté et renvoie la valeur d'index avec un datage concaténé à la fin. Un message représentant une réponse à un autre message doit utiliser **ScCreateConversationIndex** pour mettre à jour cette propriété. 
  
Un fournisseur de banque de messages permet de s'assurer que **PR_CONVERSATION_INDEX** est toujours défini sur les messages entrants ou sortants. Pour ce faire, il peut appeler **ScCreateConversationIndex**, avec la valeur existante si cette propriété est définie ou avec NULL si ce n'est pas le cas. Cette action doit être effectuée avant l'appel de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
Tous les messages qui ont la même valeur pour **PR_CONVERSATION_TOPIC** peuvent être triés sur cette propriété pour révéler la relation hiérarchique des messages. 
  
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

