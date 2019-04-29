---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438098"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une collection de clés de tri pour un tableau utilisé pour le tri standard ou par catégorie.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a>Members

 **cSorts**
  
> Nombre de structures [SSortOrder](ssortorder.md) incluses dans le membre **ASOR** . 
    
 **cCategories**
  
> Nombre de colonnes qui sont désignées en tant que colonnes de catégorie. Les valeurs possibles sont comprises entre zéro, qui indique un tri standard ou non catégorisé, et le nombre indiqué par le membre **cSorts** . 
    
 **cExpanded**
  
> Nombre de catégories qui commencent dans un état développé, où toutes les lignes qui s'appliquent à la catégorie sont visibles dans l'affichage tableau. Les valeurs possibles sont comprises entre 0 et le nombre indiqué par **cCategories**.
    
 **aSor**
  
> Tableau de structures **SSortOrder** , chacune définissant un ordre de tri. 
    
## <a name="remarks"></a>Remarques

Une structure **SSortOrderSet** est utilisée pour définir plusieurs ordres de tri pour le tri standard et catégorisé. 
  
Chaque structure **SSortOrderSet** contient au moins une structure **SSortOrder** définissant la direction du tri et la colonne qui sera utilisée comme clé de tri. Pour le tri par catégorie, cette colonne est utilisée en tant que catégorie. Lorsque la valeur du membre **cSorts** dépasse la valeur du membre **cCategories** , il y a plus de clés de tri que de Categories, et les catégories sont créées à partir des colonnes qui apparaissent en premier dans le tableau **SSortOrder** . 
  
Par exemple, si **cSorts** est défini sur 3 et **cCategories** est défini sur 2, les colonnes décrites par le membre **ulPropTag** des deux premières entrées du tableau **SSortOrder** sont utilisées comme colonnes de catégorie. La première entrée sert de groupement de catégories de niveau supérieur; deuxième entrée comme regroupement secondaire. Toutes les lignes qui correspondent aux deux colonnes de catégorie sont triées à l'aide de la clé de tri définie dans la troisième entrée. 
  
Le membre **cExpanded** spécifie le nombre de catégories qui sont développées pour la première fois. Lorsqu'il existe plusieurs catégories, l'implémentation de la table commence par la première colonne à être désignée en tant que catégorie et continue dans un ordre séquentiel avec les colonnes de catégorie suivantes jusqu'à ce que le nombre de **cCategories** ait été dépassé. S'il y a plus de colonnes de catégorie qu'il n'y a de colonnes développées, les colonnes de catégorie sont réduites. Si **cExpanded** est égal à zéro, seule la ligne d'en-tête de niveau supérieur est accessible à l'utilisateur de table pour l'affichage. Si **cExpanded** est égal à un de moins que le nombre de catégories, toutes les lignes d'en-tête et aucune des lignes de feuille sont disponibles. Si **cExpanded** est égal au nombre de catégories, le tableau est entièrement développé. 
  
Pour plus d'informations sur le tri standard et catégorisé, consultez la rubrique [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="see-also"></a>Voir aussi



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[Structures MAPI](mapi-structures.md)

