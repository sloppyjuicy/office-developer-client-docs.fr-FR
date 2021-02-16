---
title: Tri et catégorisation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418483"
---
# <a name="sorting-and-categorization"></a>Tri et catégorisation

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le tri d’un tableau place les lignes dans un ordre logique pour sa visionneuse. Par exemple, une visionneuse peut préférer voir la table des matières d’un dossier trié par objet du message afin que tous les threads d’une conversation soient ensemble, tandis qu’une autre visionneuse souhaite peut-être trier les messages par le nom de l’expéditeur. Une table nouvellement ins instantiée n’est pas nécessairement triée dans un ordre particulier. 
  
Il existe deux types de tri :
  
- Tri standard
    
- Tri catégorisé 
    
Avec le tri standard, toutes les lignes sont affichées dans une liste plate en utilisant une ou plusieurs colonnes comme clé de tri. Avec le tri catégorisé, les lignes sont affichées hiérarchiquement avec une ou plusieurs colonnes comme clé de tri. Dans chaque catégorie, il existe une ligne de titre spéciale qui contient les colonnes suivantes.
  
- Colonne ou colonnes qui font la clé de tri
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Le retrait sous la ligne de titre correspond à toutes les lignes du tableau qui contiennent des colonnes dont les valeurs correspondent à la clé de tri. Ces lignes sont appelées lignes feuilles. Les lignes de feuille contiennent toutes les colonnes du jeu de colonnes moins les colonnes de clé de tri. 
  
Les tables des matières des dossiers peuvent souvent prendre en charge le tri par catégories en plus du tri standard. Les tables de contenu des conteneurs de carnet d’adresses ne prend généralement en charge que le tri standard. 
  
Une catégorie peut avoir deux états : collapsed et expanded. Lorsqu’une catégorie est dans l’état collapsed, seule la ligne de titre est renvoyée à partir [d’IMAPITable::QueryRows](imapitable-queryrows.md). Lorsqu’une catégorie est dans l’état développé, toutes les lignes associées à la catégorie sont renvoyées. Cela inclut la ligne de titre et les lignes de feuille. 
  
Chaque catégorie d’un affichage Tableau peut être étendue ou réduire indépendamment. Autrement dit, toutes les catégories ne doivent pas être dans le même état en même temps ; Certaines catégories peuvent être réduire tandis que d’autres sont étendues. 
  
L’utilisateur d’un tableau catégorisé décide de son affichage. Une option courante consiste à utiliser un contrôle fourni dans le SDK Windows appelé contrôle Treeview. Les contrôles Treeview sont des zones de liste qui gèrent les informations dans une structure arborescence. Les lignes de titre pour les catégories dans l’état développé sont marquées avec un signe moins, tandis que les lignes de titre pour les catégories dans l’état collapsed sont marquées avec un signe plus. Les catégories étendues sont affichées avec les lignes de feuille en retrait sous les lignes de titre. 
  
Pour réduire et développer une catégorie, une application cliente ou un fournisseur de services utilise les méthodes [IMAPITable : IUnknown](imapitableiunknown.md) suivantes : 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Pour plus d’informations sur le tri des threads d’une conversation, consultez les rubriques suivantes :
  
- [SSortOrder](ssortorder.md)
    
- [Propriété canonique PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propriété canonique PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propriété canonique PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propriété canonique PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Tri des tableaux après la définition de colonnes et de restrictions](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

