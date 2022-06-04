---
title: Tri et catégorisation
description: Décrit le tri et la configuration dans Outlook 2013 et 2016. Il existe également des liens vers des documents de référence.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
ms.openlocfilehash: e6d6f12fb53d8cd7f8e904cf40ac8234c6b748b5
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894382"
---
# <a name="sorting-and-categorization"></a>Tri et catégorisation

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le tri d’une table place les lignes dans un ordre logique pour sa visionneuse. Par exemple, une visionneuse peut préférer voir la table des matières d’un dossier trié par objet de message afin que tous les threads d’une conversation soient ensemble, tandis qu’un autre utilisateur peut souhaiter que les messages soient triés par le nom de l’expéditeur. Une table nouvellement instanciée n’est pas nécessairement triée dans un ordre particulier. 
  
Il existe deux types de tri :
  
- Tri standard
    
- Tri catégorisé 
    
Avec le tri standard, toutes les lignes sont affichées dans une liste plate à l’aide d’une ou plusieurs colonnes comme clé de tri. Avec le tri catégorisé, les lignes sont affichées hiérarchiquement avec une ou plusieurs colonnes comme clé de tri. Dans chaque catégorie, il existe une ligne d’en-tête spéciale qui contient les colonnes suivantes.
  
- Colonne ou colonnes qui composent la clé de tri
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Les lignes de la table qui contiennent des colonnes avec des valeurs correspondant à la clé de tri sont mises en retrait sous la ligne de titre. Ces lignes sont appelées les lignes de feuille. Les lignes de feuille contiennent toutes les colonnes de l’ensemble de colonnes moins les colonnes de clé de tri. 
  
Les tables de contenu des dossiers prennent souvent en charge le tri catégorisé en plus du tri standard. Les tables de contenu des conteneurs de carnets d’adresses prennent généralement en charge uniquement le tri standard. 
  
Une catégorie peut avoir deux états : réduit et développé. Lorsqu’une catégorie est dans un état réduit, seule la ligne de titre est retournée par [IMAPITable::QueryRows](imapitable-queryrows.md). Lorsqu’une catégorie est dans l’état développé, toutes les lignes associées à la catégorie sont retournées. Cela inclut la ligne de titre et les lignes de feuille. 
  
Chaque catégorie d’une vue table peut être développée ou réduite indépendamment. Autrement dit, toutes les catégories ne doivent pas être dans le même état en même temps; certaines catégories peuvent être réduites tandis que d’autres sont développées. 
  
L’utilisateur d’une table classée détermine comment elle est affichée. Une option courante consiste à utiliser un contrôle fourni dans le Kit de développement logiciel (SDK) Windows appelé contrôle treeview. Les contrôles Treeview sont des zones de liste qui prennent en charge les informations dans une structure de type arborescence. Les lignes de titre pour les catégories dans l’état développé sont marquées avec un signe moins, tandis que les lignes de titre pour les catégories à l’état réduit sont marquées d’un signe plus. Les catégories développées s’affichent avec les lignes de feuille mises en retrait sous les lignes de titre. 
  
Pour réduire et développer une catégorie, une application cliente ou un fournisseur de services utilise les méthodes [IMAPITable : IUnknown](imapitableiunknown.md) suivantes : 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Pour plus d’informations sur le tri des threads d’une conversation, consultez les rubriques suivantes :
  
- [SSortOrder](ssortorder.md)
    
- [PidTagSubject Canonical, propriété](pidtagsubject-canonical-property.md)
    
- [PidTagSubjectPrefix, propriété canonique](pidtagsubjectprefix-canonical-property.md)
    
- [Propriété canonique PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propriété canonique PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Tri des tables après la définition de colonnes et de restrictions](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

