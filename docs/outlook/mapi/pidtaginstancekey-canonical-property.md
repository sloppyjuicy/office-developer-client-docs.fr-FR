---
title: Propriété canonique PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358510"
---
# <a name="pidtaginstancekey-canonical-property"></a>Propriété canonique PidTagInstanceKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui identifie de manière unique une ligne dans un tableau. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INSTANCE_KEY  <br/> |
|Identificateur :  <br/> |0x0FF6  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Tableau  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une valeur binaire qui identifie de manière unique une ligne dans un affichage Tableau. Il s’agit d’une colonne obligatoire dans la plupart des tableaux. Si une ligne est incluse dans deux affichages, il existe deux clés d’instance différentes. La clé d’instance d’une ligne peut différer chaque fois que la table est ouverte, mais reste constante pendant l’ouverture de la table. Les lignes ajoutées lors de l’utilisation d’une table ne réutilisent pas une clé d’instance précédemment utilisée. 
  
Utilisez les **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour corréler toutes les lignes d’une expansion. Utilisez **PR_INSTANCE_KEY** pour localiser une instance particulière dans l’extension. 
  
Lorsqu’une propriété à valeurs multiples est étendue dans un tableau, une ligne est créée pour chaque instance de l’extension, c’est-à-dire pour chaque valeur de cette propriété. Chaque ligne a une valeur unique pour la **propriété PR_INSTANCE_KEY,** tandis que toutes les autres colonnes conservent leurs valeurs d’origine tout au long de l’extension. 
  
Dans un tri catégorisé d’un tableau, les lignes qui ne correspondent pas aux données réelles peuvent être ajoutées au résultat du tri. Chacune de ces lignes, comme toutes les lignes de tous les tableaux, possède sa propre clé d’instance unique. 
  
 **PR_INSTANCE_KEY** est également utilisé dans les notifications d’événements de table. Les **membres propIndex** et **propPrior** de la structure [TABLE_NOTIFICATION](table_notification.md) sont des structures [SPropValue](spropvalue.md) qui PR_INSTANCE_KEY **valeurs.** Le **membre propIndex** indique la ligne qui a été ajoutée ou modifiée. Le **membre propPrior** indique la ligne avant la ligne ajoutée ou modifiée **(PR_NULL** indique une modification de la première ligne). 
  
Cette valeur n’est pas copiée dans le cadre du tableau d’affichage. 
  
 **PR_INSTANCE_KEY** est une structure [MAPIUID.](mapiuid.md) Toutes les clés d’instance peuvent être comparées directement en tant que valeurs binaires. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

