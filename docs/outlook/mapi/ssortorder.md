---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344547"
---
# <a name="ssortorder"></a>SSortOrder
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le mode de tri des lignes d'un tableau, de la colonne à utiliser comme clé de tri et de la direction du tri. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Members

**ulPropTag**
  
> Balise de propriété identifiant la clé de tri ou, pour un tri par catégorie, la colonne catégorie.
    
**ulOrder**
  
> Ordre dans lequel les données doivent être triées. Les valeurs possibles sont les suivantes:
    
  - TABLE_SORT_ASCEND: la table doit être triée par ordre croissant.
      
  - TABLE_SORT_COMBINE: l'opération de tri doit créer une catégorie qui combine la propriété identifiée en tant que colonne de clé de tri dans le membre **ulPropTag** avec la colonne de clé de tri spécifiée dans la structure **SSortOrder** précédente. 
      
    TABLE_SORT_COMBINE ne peut être utilisé que lorsque la structure **SSortOrder** est utilisée comme entrée dans une structure [SSortOrderSet](ssortorderset.md) pour spécifier plusieurs ordres de tri pour un tri catégorisé. TABLE_SORT_COMBINE ne peut pas être utilisé dans la première structure **SSortOrder** dans une structure **SSortOrderSet** . 
      
  - TABLE_SORT_DESCEND: le tableau doit être trié dans l'ordre décroissant.
      
  - TABLE_SORT_CATEG_MAX: le tableau doit être trié sur la valeur maximale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l'ordre de tri précédent dans la structure **SSortOrderSet** . 
      
  - TABLE_SORT_CATEG_MIN: le tableau doit être trié sur la valeur minimale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l'ordre de tri précédent dans la structure **SSortOrderSet** . 
    
## <a name="remarks"></a>Remarques

Une structure **SSortOrder** est utilisée pour décrire comment effectuer une opération de tri standard ou une opération de tri catégorisé. Les structures **SSortOrder** sont généralement combinées en une structure **SSortOrderSet** pour décrire plusieurs clés et itinéraires de tri. Les structures **SSortOrderSet** sont utilisées dans les fonctions et méthodes d'interface suivantes: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
La plage de colonnes autorisées dans une table qui peut être utilisée en tant que clé de tri dépend du fournisseur. Les colonnes qui font partie du jeu de colonnes actuel peuvent toujours être utilisées en tant que clés de tri. Toutefois, chaque fournisseur détermine si les clés de tri peuvent être définies à l'aide des colonnes disponibles qui ne figurent pas dans le jeu de colonnes actuel. Une colonne disponible est une colonne qui est renvoyée à partir de l'option [IMAPITable:: QueryColumns](imapitable-querycolumns.md) lorsque l'indicateur TBL_ALL_COLUMNS est défini. 
  
Le membre **ulOrder** indique les informations d'ordre directionnel et de catégorisation, par exemple, par conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), c'est-à-dire, le fil de conversation, qui est une série de messages et de réponses. Les lignes peuvent être triées dans l'ordre croissant ou décroissant avec toutes les entrées NULL positionnées en dernier. 
  
La valeur TABLE_SORT_COMBINE indique que la colonne spécifiée dans **ulPropTag** doit être combinée à la colonne de catégorie précédente pour former une catégorie composite. Autrement dit, au lieu de classer les valeurs uniques des colonnes, TABLE_SORT_COMBINE autorise la catégorisation sur les valeurs uniques d'une combinaison de colonnes. Par exemple, une catégorie unique peut être définie pour regrouper les messages reçus d'un expéditeur particulier sur un sujet particulier. La définition de la valeur sur TABLE_SORT_COMBINE réduit le nombre de lignes de catégorie affichées. 
  
Le tri sur des colonnes à valeurs multiples n'est pas pris en charge de façon universelle par toutes les implémentations de table. S'il est pris en charge, appliquez l'MV_FLAG à l'aide de la macro MVI_PROP à la balise de propriété dans le membre **ulPropTag** pour identifier la clé de tri en tant que colonne à valeurs multiples. Le tri sur une colonne à valeurs multiples est basé sur l'utilisation des valeurs individuelles. 
  
> [!IMPORTANT]
> Les valeurs de membre de **ULORDER** TABLE_SORT_CATEG_MAX et TABLE_SORT_CATEG_MIN ne peuvent pas être définies dans le fichier d'en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l'ajouter à votre code en utilisant les valeurs suivantes: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Pour plus d'informations sur le tri standard et catégorisé, consultez la rubrique [Tri et catégorisation](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Voir aussi

- [SSortOrderSet](ssortorderset.md)
- [Structures MAPI](mapi-structures.md)

