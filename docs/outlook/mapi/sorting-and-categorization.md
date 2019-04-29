---
title: Tri et catégorisation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418483"
---
# <a name="sorting-and-categorization"></a>Tri et catégorisation

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Trier un tableau place les lignes dans un ordre approprié pour la visionneuse. Par exemple, une visionneuse peut préférer consulter la table des matières d'un dossier triée par objet de message de sorte que tous les threads d'une conversation soient réunis tandis qu'une autre peut souhaiter que les messages soient triés en fonction du nom de l'expéditeur. Une table nouvellement instanciée n'est pas nécessairement triée dans un ordre particulier. 
  
Il existe deux types de tri:
  
- Tri standard
    
- Tri par catégorie 
    
Avec le tri standard, toutes les lignes s'affichent dans une liste plate à l'aide d'une ou de plusieurs colonnes en tant que clé de tri. Avec le tri par catégorie, les lignes sont affichées hiérarchiquement avec une ou plusieurs colonnes en tant que clé de tri. Dans chaque catégorie, il existe une ligne d'en-tête spéciale qui contient les colonnes suivantes.
  
- La ou les colonnes qui composent la clé de tri
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Le retrait sous la ligne d'en-tête contient toutes les lignes de la table qui contiennent des colonnes avec des valeurs qui correspondent à la clé de tri. Ces lignes sont appelées lignes feuille. Les lignes de feuille contiennent toutes les colonnes de l'ensemble de colonnes moins les colonnes de clés de tri. 
  
Les tables de contenu des dossiers prennent généralement en charge le tri par catégorie en plus du tri standard. Les tables de contenu des conteneurs du carnet d'adresses prennent généralement en charge uniquement le tri standard. 
  
Une catégorie peut avoir deux États: réduite et développée. Lorsqu'une catégorie est réduite, seule la ligne d'en-tête est renvoyée à partir de l'état [IMAPITable:: QueryRows](imapitable-queryrows.md). Lorsqu'une catégorie est dans l'état développé, toutes les lignes associées à la catégorie sont renvoyées. Cela inclut la ligne d'en-tête et les lignes de feuille. 
  
Chaque catégorie dans un affichage tableau peut être développée ou réduite indépendamment. Autrement dit, toutes les catégories ne doivent pas être dans le même État en même temps; certaines catégories peuvent être réduites, tandis que d'autres sont développées. 
  
L'utilisateur d'un tableau classé détermine son mode d'affichage. Une option commune consiste à utiliser un contrôle fourni dans le kit de développement logiciel (SDK) Windows appelé contrôle TreeView. Les contrôles TreeView sont des zones de liste qui prennent en charge les informations dans une structure arborescente. Les lignes d'en-tête pour les catégories dans l'état développé sont signalées par un signe moins tandis que les lignes de titre pour les catégories dans l'État réduit sont signalées par un signe plus. Les catégories développées sont affichées avec les lignes de feuille mises en retrait sous les lignes d'en-tête. 
  
Pour réduire et développer une catégorie, une application cliente ou un fournisseur de services utilise la méthode [IMAPITable suivante: méthodes IUnknown](imapitableiunknown.md) : 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Pour plus d'informations sur le tri des threads d'une conversation, consultez les rubriques suivantes:
  
- [SSortOrder](ssortorder.md)
    
- [Propriété canonique PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propriété canonique PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propriété canonique PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propriété canonique PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Tri des tables après la définition des colonnes et des restrictions](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

