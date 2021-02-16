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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439722"
---
# <a name="ssortorder"></a>SSortOrder
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le mode de tri des lignes d’un tableau, la colonne à utiliser comme clé de tri et le sens du tri. 
  
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

## <a name="members"></a>Members

**ulPropTag**
  
> Balise de propriété identifiant la clé de tri ou, pour un tri catégorisé, la colonne de catégorie.
    
**ulOrder**
  
> Ordre dans lequel les données doivent être triées. Les valeurs possibles sont les ci-après :
    
  - TABLE_SORT_ASCEND : le tableau doit être trié par ordre croissant.
      
  - TABLE_SORT_COMBINE : l’opération de tri doit créer une catégorie qui combine la propriété identifiée en tant que colonne de clé de tri dans le membre **ulPropTag** avec la colonne de clé de tri spécifiée dans la structure **SSortOrder** précédente. 
      
    TABLE_SORT_COMBINE ne peut être utilisé que lorsque la structure **SSortOrder** est utilisée comme entrée dans une structure [SSortOrderSet](ssortorderset.md) pour spécifier plusieurs ordres de tri pour un tri classé. TABLE_SORT_COMBINE ne peut pas être utilisé dans la première structure **SSortOrder** d’une structure **SSortOrderSet.** 
      
  - TABLE_SORT_DESCEND : le tableau doit être trié dans l’ordre décroit.
      
  - TABLE_SORT_CATEG_MAX : le tableau doit être trié sur la valeur maximale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédent dans la structure **SSortOrderSet.** 
      
  - TABLE_SORT_CATEG_MIN : le tableau doit être trié sur la valeur minimale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédent dans la structure **SSortOrderSet.** 
    
## <a name="remarks"></a>Remarques

Une structure **SSortOrder** est utilisée pour décrire comment effectuer une opération de tri standard ou une opération de tri classée. Les structures **SSortOrder** sont généralement combinées dans une structure **SSortOrderSet** pour décrire plusieurs directions et clés de tri. Les structures **SSortOrderSet** sont utilisées dans les fonctions et méthodes d’interface suivantes : 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
La plage de colonnes autorisées dans un tableau qui peut être utilisée comme clé de tri dépend du fournisseur. Les colonnes qui font partie du jeu de colonnes actuel peuvent toujours être utilisées comme clés de tri. Toutefois, chaque fournisseur détermine si les clés de tri peuvent être définies à l’aide des colonnes disponibles qui ne sont pas dans le jeu de colonnes actuel. Une colonne disponible est une colonne renvoyée par [IMAPITable::QueryColumns](imapitable-querycolumns.md) lorsque l’TBL_ALL_COLUMNS est définie. 
  
Le **membre ulOrder** indique à la fois l’ordre directionnel et les informations de catégorisation, par exemple, par conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), autrement dit, thread de conversation, qui est une série de messages et de réponses. Les lignes peuvent être triées dans une séquence descendante ou ascendante avec toutes les entrées NULL positionnées en dernier. 
  
La TABLE_SORT_COMBINE indique que la colonne spécifiée dans **ulPropTag** doit être combinée avec la colonne de catégorie précédente pour former une catégorie composite. Autrement dit, au lieu de catégoriser des valeurs uniques de colonnes individuelles, TABLE_SORT_COMBINE permet la catégorisation des valeurs uniques d’une combinaison de colonnes. Par exemple, une catégorie unique peut être définie pour grouper les messages reçus d’un expéditeur particulier sur un sujet particulier. Définir la valeur sur TABLE_SORT_COMBINE réduit le nombre de lignes de catégorie affichées. 
  
Le tri sur des colonnes à valeurs multiples n’est pas universellement pris en charge par toutes les implémentations de tableau. Si elle est prise en charge, appliquez la MV_FLAG à l’aide de la macro MVI_PROP à la balise de propriété dans le membre **ulPropTag** pour identifier la clé de tri en tant que colonne à valeurs multiples. Le tri sur une colonne à valeurs multiples est basé sur l’utilisation des valeurs individuelles. 
  
> [!IMPORTANT]
> Les valeurs de membre **ulOrder** TABLE_SORT_CATEG_MAX et TABLE_SORT_CATEG_MIN peuvent ne pas être définies dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Pour plus d’informations sur le tri standard et catégorisé, voir [Tri et catégorisation.](sorting-and-categorization.md) 
  
## <a name="see-also"></a>Voir aussi

- [SSortOrderSet](ssortorderset.md)
- [Structures MAPI](mapi-structures.md)

