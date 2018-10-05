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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396987"
---
# <a name="pidtaginstancekey-canonical-property"></a>Propriété canonique PidTagInstanceKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui identifie de manière unique une ligne dans une table. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_INSTANCE_KEY  <br/> |
|Identificateur :  <br/> |0x0FF6  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Table  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une valeur binaire qui identifie de manière unique une ligne dans une table. Il est une colonne requise dans la plupart des tables. Si une ligne est incluse dans les deux modes, il existe deux clés instance différente. La clé de l’instance d’une ligne peut varier chaque fois que la table est ouverte, mais reste constante lors de la table est ouverte. Lignes ajoutées pendant une table est en cours d’utilisation ne réutilisez pas une clé d’instance qui a été utilisée précédemment. 
  
Utilisez la **propriété PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou des propriétés de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour faire correspondre toutes les lignes d’une expansion. Utilisez **PR_INSTANCE_KEY** pour rechercher une instance spécifique au sein de l’extension. 
  
Lorsque vous développez une propriété à valeurs multiples dans une table, une ligne est créée pour chaque instance de l’extension, en autrement dit, pour chaque valeur de cette propriété. Chaque ligne a une valeur unique pour la propriété **PR_INSTANCE_KEY** , tandis que toutes les autres colonnes conservent leurs valeurs d’origine dans le développement. 
  
Dans un tri par catégorie d’un tableau, les lignes ne correspondant ne pas à des données réelles peuvent être ajoutées au résultat du tri. Chaque ligne ce, tels que toutes les lignes de toutes les tables, possède sa propre clé d’instance unique. 
  
 **PR_INSTANCE_KEY** est également utilisée dans les notifications d’événement table. Les membres **propIndex** et **propPrior** de la structure [TABLE_NOTIFICATION](table_notification.md) sont des structures [SPropValue](spropvalue.md) contenant des valeurs **PR_INSTANCE_KEY** . Le membre **propIndex** indique la ligne qui a été ajoutée ou modifiée. Le membre **propPrior** indique la ligne avant la ligne ajoutée ou modifiée (**PR_NULL** indique une modification apportée à la première ligne). 
  
Cette valeur n’est pas copiée dans le cadre de la table d’affichage. 
  
 **PR_INSTANCE_KEY** est une structure [MAPIUID](mapiuid.md) . Toutes les clés de l’instance peuvent être comparées directement en tant que valeurs binaires. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

