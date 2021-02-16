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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422893"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère toutes les lignes d’un tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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

 _ptable_
  
> [in] Pointeur vers la table MAPI à partir de laquelle les lignes sont récupérées. 
    
 _ptaga_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant des colonnes de tableau. Ces balises sont utilisées pour sélectionner les colonnes spécifiques à récupérer. Si le _paramètre ptaga_ est NULL, **HrQueryAllRows** récupère l’ensemble de colonnes entier de la vue de table actuelle transmise dans le _paramètre ptable._ 
    
 _pres_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) qui contient des restrictions de récupération. Si le  _paramètre pres_ est NULL, **HrQueryAllRows ne** fait aucune restriction. 
    
 _psos_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) identifiant l’ordre de tri des colonnes à récupérer. Si le  _paramètre psos_ est NULL, l’ordre de tri par défaut du tableau est utilisé. 
    
 _maxsMax_
  
> [in] Nombre maximal de lignes à récupérer. Si la valeur du paramètre  _« zero_ » est zéro, aucune limite n’est définie sur le nombre de lignes récupérées. 
    
 _pprows_
  
> [out] Pointeur vers un pointeur vers la structure [SRowSet](srowset.md) renvoyée qui contient un tableau de pointeurs vers les lignes de tableau récupérées. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a récupéré les lignes attendues d’un tableau. 
    
MAPI_E_TABLE_TOO_BIG 
  
> Le nombre de lignes du tableau est supérieur au nombre passé pour le _paramètremax._ 
    
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services n’a aucun contrôle sur le nombre de lignes que **HrQueryAllRows** tente d’extraire, autrement qu’en élisant une restriction pointée par le paramètre _pres._ Le  _paramètre parcsMax_ ne limite pas la récupération à un certain nombre de lignes de tableau, mais définit plutôt une quantité maximale de mémoire disponible pour contenir toutes les lignes récupérées. La seule protection contre le dépassement de mémoire massive est la fonctionnalité stopgap fournie par la définition de _la fonctionmax._ Le retour d’MAPI_E_TABLE_TOO_BIG signifie que le tableau contient trop de lignes pour être maintenues en mémoire en même temps. 
  
Les tables généralement de petite taille, telles qu’une table de magasins de messages ou une table de fournisseurs, peuvent généralement être récupérées en toute sécurité avec **HrQueryAllRows**. Les tables à risque d’être très grandes, telles qu’une table des matières ou même une table des destinataires, doivent être parcourues dans des sous-sections à l’aide de la méthode [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
Si des propriétés de table ne sont pas définies lors de l’appel de **HrQueryAllRows,** elles sont renvoyées avec le type de propriété PT_NULL et l’identificateur de PROP_ID_NULL 
  

