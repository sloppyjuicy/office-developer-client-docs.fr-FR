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
  
Récupère toutes les lignes d'un tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

 _pTable_
  
> dans Pointeur vers la table MAPI à partir de laquelle les lignes sont extraites. 
    
 _ptaga_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant des colonnes de tableau. Ces balises sont utilisées pour sélectionner les colonnes spécifiques à récupérer. Si le paramètre _ptaga_ est null, **HrQueryAllRows** récupère le jeu de colonnes entier de la vue de table actuelle passée dans le paramètre _pTable_ . 
    
 _avance_
  
> dans Pointeur vers une structure [SRestriction](srestriction.md) qui contient des restrictions de récupération. Si le paramètre _pres_ est null, **HrQueryAllRows** n'impose aucune restriction. 
    
 _PSOS_
  
> dans Pointeur vers une structure [SSortOrderSet](ssortorderset.md) identifiant l'ordre de tri des colonnes à récupérer. Si le paramètre _PSOS_ est null, l'ordre de tri par défaut de la table est utilisé. 
    
 _crowsMax_
  
> dans Nombre maximal de lignes à récupérer. Si la valeur du paramètre _crowsMax_ est égale à zéro, aucune limite n'est définie pour le nombre de lignes extraites. 
    
 _ppRows_
  
> remarquer Pointeur vers un pointeur vers la structure [SRowSet](srowset.md) renvoyée qui contient un tableau de pointeurs vers les lignes de tableau récupérées. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a extrait les lignes attendues d'un tableau. 
    
MAPI_E_TABLE_TOO_BIG 
  
> Le nombre de lignes dans le tableau est supérieur au nombre passé pour le paramètre _crowsMax_ . 
    
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services ne contrôle pas le nombre de lignes **HrQueryAllRows** tente de récupérer, à l'exception du fait qu'il impose une restriction vers laquelle pointe le paramètre _pres_ . Le paramètre _crowsMax_ ne limite pas la récupération à un certain nombre de lignes de tableau, mais définit plutôt une quantité maximale de mémoire disponible pour contenir toutes les lignes extraites. La seule protection contre le débordement de mémoire massive est la fonctionnalité stopgap fournie par la définition de _crowsMax_. L'erreur Return MAPI_E_TABLE_TOO_BIG signifie que le tableau contient trop de lignes à conserver en une seule fois dans la mémoire. 
  
Les tables généralement petites, comme une table de banque de messages ou une table de fournisseurs, peuvent généralement être récupérées en toute sécurité avec **HrQueryAllRows**. Les tables susceptibles d'être très volumineuses, telles qu'une table des matières ou même une table de destinataires, doivent être parcourues dans des sous-sections à l'aide de la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Si les propriétés d'une table ne sont pas définies lors de l'appel de **HrQueryAllRows** , elles sont renvoyées avec le type de propriété PT_NULL et l'identificateur de propriété PROP_ID_NULL 
  

