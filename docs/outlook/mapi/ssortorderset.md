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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e8d85ba55c5aa2f3780ad8e04cf1326cd7c35865
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575937"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une collection de clés de tri pour une table qui est utilisé pour le tri standard ou par catégorie.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
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
  
> Nombre de structures [SSortOrder](ssortorder.md) qui sont inclus dans le membre **aSort** . 
    
 **cCategories**
  
> Nombre de colonnes qui sont désignés en tant que colonnes de la catégorie. Plage de valeurs possibles à partir de zéro, ce qui indique un tri standard ou non classés, au numéro indiqué par le membre **cSorts** . 
    
 **cExpanded**
  
> Nombre de catégories qui démarre dans un état développé, où toutes les lignes qui s’appliquent à la catégorie sont visibles dans l’affichage tableau. Valeurs possibles sont comprises entre 0 et le nombre indiqué par **cCategories**.
    
 **aSort**
  
> Tableau de structures **SSortOrder** , chaque définition d’un ordre de tri. 
    
## <a name="remarks"></a>Remarques

Une structure **SSortOrderSet** est utilisée pour définir plusieurs ordres de tri pour le tri standard et par catégorie. 
  
Chaque structure **SSortOrderSet** contient au moins une structure **SSortOrder** définit la direction de l’ordre de tri et de la colonne qui sera utilisée comme clé de tri. Pour le tri par catégorie, cette colonne est utilisée en tant que la catégorie. Lorsque la valeur du membre **cSorts** dépasse la valeur du membre **cCategories** , il existe plusieurs clés de tri que les catégories et les catégories sont créées à partir des colonnes qui s’affichent en premier dans le tableau **SSortOrder** . 
  
Par exemple, si **cSorts** est défini à 3 et **cCategories** est défini sur 2, les colonnes décrites par le membre **ulPropTag** les deux premières entrées dans le tableau **SSortOrder** sont utilisées comme colonnes de catégorie. La première entrée sert de la catégorie de niveau supérieur de regroupement ; la deuxième entrée en tant que le groupe secondaire. Toutes les lignes qui correspondent aux colonnes deux catégories sont triés à l’aide de la clé de tri définie dans la troisième entrée. 
  
Le membre **cExpanded** Spécifie le nombre de catégories qui sont développés dans un premier temps. Lorsqu’il existe plusieurs catégories, l’implémentation de la table commence par la première colonne à désigner comme une catégorie et continue dans l’ordre séquentiel avec les colonnes de catégorie suivantes jusqu'à ce que le nombre de **cCategories** a été dépassé. S’il n’y a plus de colonnes de catégorie que l’étendue de colonnes, les colonnes de la catégorie sont réduits. Si **cExpanded** est égale à zéro, uniquement la ligne d’en-tête de niveau supérieur est disponible à l’utilisateur de la table pour l’affichage. Si **cExpanded** est égale à moins que le nombre d’abscisses, toutes les lignes d’en-tête et aucune des lignes de feuille sont disponibles. Si **cExpanded** est égal au nombre de catégories, le tableau est développé. 
  
Pour plus d’informations sur le tri standard et par catégorie, voir [tri et catégorisation](sorting-and-categorization.md).
  
## <a name="see-also"></a>Voir aussi



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[Structures MAPI](mapi-structures.md)

