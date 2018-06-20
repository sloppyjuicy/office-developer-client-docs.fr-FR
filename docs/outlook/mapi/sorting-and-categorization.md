---
title: Tri et classement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 5e63d276d25a26f937e9b4f44575fea1030f52d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787209"
---
# <a name="sorting-and-categorization"></a>Tri et classement

 
  
**S’applique à**: Outlook 
  
Tri d’un tableau place les lignes dans un ordre significatif pour la visionneuse. Par exemple, une visionneuse pourrait être préférable de voir la table des matières d’un dossier trié par objet du message, afin que tous les threads d’une conversation ensemble pendant une autre visionneuse souhaiterez les messages triés par le nom de l’expéditeur. Une table nouvellement instanciée n’est pas nécessairement triée selon un ordre particulier. 
  
Il existe deux types de tri :
  
- Tri standard
    
- Classés tri 
    
Tri standard, toutes les lignes sont affichées dans une liste simple à l’aide d’une ou plusieurs colonnes comme clé de tri. Tri par catégorie, les lignes sont affichés hiérarchiquement avec une ou plusieurs colonnes comme clé de tri. Dans chaque catégorie, il est une ligne d’en-tête spécial qui contient les colonnes suivantes.
  
- L’ou les colonnes qui constituent la clé de tri
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Mis en retrait sous la ligne d’en-tête sont toutes les lignes de la table contenant des colonnes avec des valeurs qui correspondent à la clé de tri. Ces lignes sont appelées les lignes de feuille. Lignes de feuille contient toutes les colonnes dans la colonne valeur moins les colonnes de clés de tri. 
  
Les tables de contenu des dossiers prennent généralement en charge le tri par catégorie en plus de tri standard. Les tables de contenu des conteneurs de carnet d’adresses prennent généralement en charge uniquement le tri standard. 
  
Une catégorie peut avoir deux états : réduits et développés. Lorsqu’une catégorie est dans l’état réduit, la ligne d’en-tête est renvoyée à partir de [IMAPITable::QueryRows](imapitable-queryrows.md). Lorsqu’une catégorie est dans l’état développé, toutes les lignes associées à la catégorie sont renvoyés. Cela inclut la ligne d’en-tête et les lignes de feuille. 
  
Chaque catégorie dans un affichage tableau peut être développé ou réduit de manière indépendante. Autrement dit, pas toutes les catégories doivent être dans le même état en même temps ; des catégories peuvent être réduits tandis que d’autres personnes sont développés. 
  
L’utilisateur d’une table, voir décide comment il est affiché. Une option commune consiste à utiliser un contrôle fourni dans le SDK de Windows appelée le contrôle treeview. Contrôles TreeView sont les zones de liste qui prennent en charge les informations dans une structure d’arborescence. Lignes d’en-tête pour les catégories dans l’état développé sont marqués avec un signe moins, tandis que les lignes d’en-tête pour les catégories dans l’état réduit sont marquées avec un signe plus. Catégories de l’étendue sont affichés avec les lignes de feuille en retrait sous les lignes d’en-tête. 
  
Pour réduire et développer une catégorie, une application cliente ou un fournisseur de services utilise les éléments suivants [IMAPITable : IUnknown](imapitableiunknown.md) méthodes : 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Pour plus d’informations sur le tri, les threads d’une conversation voir les rubriques suivantes :
  
- [SSortOrder](ssortorder.md)
    
- [Propriété canonique PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propriété canonique PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propriété canonique PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propriété canonique PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Tri des tableaux après avoir défini les Restrictions et les colonnes](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

