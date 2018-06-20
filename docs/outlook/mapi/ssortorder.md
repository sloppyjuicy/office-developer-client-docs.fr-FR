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
ms.openlocfilehash: 7cb511c7a021c4e65214acc7efa785be0e02ffc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787245"
---
# <a name="ssortorder"></a>SSortOrder
 
**S’applique à**: Outlook 
  
Définit comment trier les lignes d’une table, une colonne à utiliser comme la clé de tri et le sens du tri. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Membres

**ulPropTag**
  
> Balise de propriété identifiant le tri clé ou, pour un tri par catégorie, la colonne catégorie.
    
**ulOrder**
  
> L’ordre dans lequel les données sont à trier. Les valeurs possibles sont les suivantes :
    
  - TABLE_SORT_ASCEND : Le tableau doit être trié par ordre croissant.
      
  - TABLE_SORT_COMBINE : L’opération de tri doit créer une catégorie qui associe la propriété identifiée en tant que colonne de clé de tri dans le membre **ulPropTag** avec la colonne de clé de tri spécifiée dans la structure **SSortOrder** précédente. 
      
    TABLE_SORT_COMBINE peut être utilisé uniquement lorsque la structure **SSortOrder** est utilisée comme une entrée dans une structure [SSortOrderSet](ssortorderset.md) pour spécifier plusieurs ordres de tri pour un tri par catégorie. TABLE_SORT_COMBINE ne peut pas être utilisé dans la première structure **SSortOrder** dans une structure **SSortOrderSet** . 
      
  - TABLE_SORT_DESCEND : Le tableau doit être trié par ordre décroissant.
      
  - TABLE_SORT_CATEG_MAX : Le tableau doit être trié sur la valeur maximale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédente dans la structure **SSortOrderSet** . 
      
  - TABLE_SORT_CATEG_MIN : Le tableau doit être trié sur la valeur minimale du membre pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédente dans la structure **SSortOrderSet** en **ulPropTag** . 
    
## <a name="remarks"></a>Remarques

Une structure **SSortOrder** est utilisée pour décrire comment effectuer une opération de tri standard ou une opération de tri par catégorie. Structures **SSortOrder** sont généralement combinées en une structure **SSortOrderSet** pour décrire plusieurs clés de tri et des instructions. Structures **SSortOrderSet** sont utilisés dans les méthodes d’interface les fonctions suivantes : 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
La plage de colonnes autorisés dans une table qui peut être utilisé comme une clé de tri dépend du fournisseur. Colonnes qui font partie de l’ensemble actuel de la colonne peuvent toujours être utilisés en tant que clés de tri. Toutefois, chaque fournisseur détermine si les clés de tri peuvent être définis à l’aide des colonnes disponibles sont définies pas dans la colonne en cours. Une colonne disponible est une colonne qui est renvoyée à partir de [IMAPITable::QueryColumns](imapitable-querycolumns.md) lors de l’indicateur TBL_ALL_COLUMNS est défini. 
  
Le membre **ulOrder** indique à la fois ordre direction et informations de catégorisation, par exemple, par conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), c'est-à-dire conversationnel thread, ce qui est une série de messages et des réponses. Lignes peuvent être triés dans un croissant ou décroissant séquence avec toutes les entrées NULL placées en dernier. 
  
La valeur TABLE_SORT_COMBINE indique que la colonne spécifiée dans **ulPropTag** doit être combinée avec la colonne catégorie précédente afin de former une catégorie composite. Autrement dit, au lieu de classement des valeurs uniques de colonnes individuelles, TABLE_SORT_COMBINE permet la catégorisation des valeurs uniques d’une combinaison de colonnes. Par exemple, une seule catégorie peut être définie pour regrouper les messages provenant d’un expéditeur particulier sur un sujet particulier. La valeur TABLE_SORT_COMBINE réduit le nombre de lignes de catégorie qui sont affichés. 
  
Tri des colonnes à valeurs multiples n’est pas universel pris en charge par toutes les implémentations de tableau. Si prise en charge, appliquer la MV_FLAG à l’aide de la macro MVI_PROP à la balise de propriété dans le membre **ulPropTag** pour identifier la clé de tri dans une colonne à valeurs multiples. Tri sur une colonne à valeurs multiples est basé sur l’utilisation des valeurs. 
  
> [!IMPORTANT]
> Les valeurs de membre **ulOrder** TABLE_SORT_CATEG_MAX et TABLE_SORT_CATEG_MIN ne peuvent pas être définis dans le fichier d’en-tête téléchargeable est actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Pour plus d’informations sur le tri standard et par catégorie, voir [tri et catégorisation](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Voir aussi

- [SSortOrderSet](ssortorderset.md)
- [Structures MAPI](mapi-structures.md)

