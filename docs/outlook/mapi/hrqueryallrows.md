---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783563"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**S’applique à**: Outlook 
  
Récupère toutes les lignes d’une table. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a>Paramètres

 _pTable_
  
> [in] Pointeur vers le tableau MAPI à partir de laquelle les lignes sont extraites. 
    
 _ptaga_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de propriété balises indiquant des colonnes de tableau. Ces balises sont utilisées pour sélectionner les colonnes spécifiques à récupérer. Si le paramètre _ptaga_ est NULL, **HrQueryAllRows** récupère l’ensemble de la colonne entière de l’affichage tableau actuel passé dans le paramètre _ptable_ . 
    
 _Appuyez_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) qui contient les restrictions de récupération. Si le paramètre _Appuyez_ est NULL, **HrQueryAllRows** n’apporte aucune restriction. 
    
 _PSO_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui identifie l’ordre de tri des colonnes à récupérer. Si le paramètre _PSO_ est NULL, l’ordre de tri par défaut pour la table est utilisée. 
    
 _crowsMax_
  
> [in] Nombre maximal de lignes à récupérer. Si la valeur du paramètre _crowsMax_ est égale à zéro, aucune limite sur le nombre de lignes extraites n’est définie. 
    
 _ppRows_
  
> [out] Pointeur vers un pointeur vers la structure [SRowSet](srowset.md) retournée qui contient un tableau de pointeurs vers les lignes du tableau récupéré. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel extraire les lignes d’un tableau attendus. 
    
MAPI_E_TABLE_TOO_BIG 
  
> Le nombre de lignes dans le tableau est supérieur à la valeur transmise au paramètre _crowsMax_ . 
    
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services ne contrôle pas le nombre de lignes **que HrQueryAllRows** tente de récupérer, autres qu’en imposant une restriction vers laquelle pointe le paramètre _Appuyez_ . Le paramètre _crowsMax_ ne limite pas la récupération à un certain nombre de lignes du tableau, mais plutôt définit une quantité maximale de mémoire disponible pour contenir les lignes récupérées toutes les. La seule protection contre le dépassement de capacité de mémoire RAM très importante est la fonctionnalité provisoires fournie par le paramètre _crowsMax_. L’erreur renvoyée MAPI_E_TABLE_TOO_BIG signifie que le tableau contient trop de lignes pour qu’il ait en une seule fois dans la mémoire. 
  
Tables qui sont généralement petites, par exemple un magasin de la table message ou un fournisseur généralement peuvent être en toute sécurité récupérés par **HrQueryAllRows**. Tables risque d’être très volumineuses, par exemple une table des matières ou même une table de destinataires, doivent être parcourues dans les sous-sections à l’aide de la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) . 
  
Si les propriétés du tableau ne sont pas définies lorsque **HrQueryAllRows** est appelée, ils sont retournées avec le type de la propriété PT_NULL et l’identificateur de la propriété PROP_ID_NULL 
  

