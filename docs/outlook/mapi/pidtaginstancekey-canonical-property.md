---
title: Propriété canonique PidTagInstanceKey
description: Cet article décrit la propriété canonique PidTagInstanceKey, qui contient une valeur qui identifie de façon unique une ligne dans une table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
ms.openlocfilehash: 5361ae0e08d6d023d3a49e0785ae52556a2def94
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752357"
---
# <a name="pidtaginstancekey-canonical-property"></a>Propriété canonique PidTagInstanceKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui identifie de façon unique une ligne dans une table. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INSTANCE_KEY  <br/> |
|Identificateur :  <br/> |0x0FF6  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Tableau  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une valeur binaire qui identifie de façon unique une ligne dans une vue de table. Il s’agit d’une colonne obligatoire dans la plupart des tables. Si une ligne est incluse dans deux vues, il existe deux clés d’instance différentes. La clé d’instance d’une ligne peut différer chaque fois que la table est ouverte, mais reste constante pendant l’ouverture de la table. Les lignes ajoutées pendant l’utilisation d’une table ne réutilisent pas une clé d’instance précédemment utilisée. 
  
Utilisez les propriétés **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour mettre en corrélation toutes les lignes d’une expansion. Utilisez **PR_INSTANCE_KEY** pour localiser une instance particulière dans l’extension. 
  
Lorsqu’une propriété à valeurs multiples est développée dans une table, une ligne est créée pour chaque instance de l’extension, c’est-à-dire pour chaque valeur de cette propriété. Chaque ligne a une valeur unique pour la propriété **PR_INSTANCE_KEY** , tandis que toutes les autres colonnes conservent leurs valeurs d’origine tout au long de l’expansion. 
  
Dans un type catégorisé d’une table, les lignes qui ne correspondent pas aux données réelles peuvent être ajoutées au résultat du tri. Chaque ligne de ce type, comme toutes les lignes de toutes les tables, a sa propre clé d’instance unique. 
  
 **PR_INSTANCE_KEY** est également utilisé dans les notifications d’événements de table. Les membres **propIndex** et **propPrior** de la structure [TABLE_NOTIFICATION](table_notification.md) sont des structures [SPropValue](spropvalue.md) contenant des valeurs **PR_INSTANCE_KEY** . Le **membre propIndex** indique la ligne qui a été ajoutée ou modifiée. Le membre **propPrior** indique la ligne avant la ligne ajoutée ou modifiée (**PR_NULL** indique une modification de la première ligne). 
  
Cette valeur n’est pas copiée dans le cadre de la table d’affichage. 
  
 **PR_INSTANCE_KEY** est une structure [MAPIUID](mapiuid.md) . Toutes les clés d’instance peuvent être directement comparées en tant que valeurs binaires. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d’utilisateurs, de contacts, de groupes et de ressources.
    
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

