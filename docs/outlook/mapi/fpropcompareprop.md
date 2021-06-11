---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427156"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété à l’aide d’un opérateur relationnel spécifié. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parameters

_lpSPropValue1_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la première valeur de propriété à comparer. 
    
_ulRelOp_
  
> [in] Opérateur relationnel à utiliser dans la comparaison. Pour les valeurs permises, voir la structure [SComparePropsRestriction.](scomparepropsrestriction.md) 
    
_lpSPropValue2_
  
> [in] Pointeur vers une structure **SPropValue** définissant la deuxième valeur de propriété à comparer. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Les valeurs de propriété répondent à la relation spécifiée. 
    
FALSE 
  
> Les valeurs de propriété ne répondent pas à la relation spécifiée.
    
## <a name="remarks"></a>Remarques

La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de [propriétéSPropValue.](spropvalue.md) Les **fonctions FPropCompareProp** et [FPropContainsProp](fpropcontainsprop.md) peuvent être utilisées pour préparer les restrictions de génération d’une table. 
  
L’ordre de comparaison est  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Si les types de propriété des valeurs de propriété à comparer ne correspondent pas, la **fonction FPropCompareProp** renvoie false. 
  

