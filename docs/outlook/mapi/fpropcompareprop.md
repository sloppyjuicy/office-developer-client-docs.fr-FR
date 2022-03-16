---
title: FPropCompareProp
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: Compare deux valeurs de propriété à l’aide d’un opérateur relationnel spécifié.
ms.openlocfilehash: f94cad0854c496773837da5b3b4f06cb22532557
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507870"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**S’applique à** : Outlook 2013 | Outlook 2016
  
Compare deux valeurs de propriété à l’aide d’un opérateur relationnel spécifié.
  
|**Valeur**|**Description**|
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

## <a name="parameters"></a>Paramètres

_lpSPropValue1_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la première valeur de propriété à comparer.

_ulRelOp_
  
> [in] Opérateur relationnel à utiliser dans la comparaison. Pour les valeurs permises, voir [la structure SComparePropsRestriction](scomparepropsrestriction.md) .

_lpSPropValue2_
  
> [in] Pointeur vers une structure **SPropValue** définissant la deuxième valeur de propriété à comparer.

## <a name="return-value"></a>Valeur renvoyée

TRUE
  
> Les valeurs de propriété répondent à la relation spécifiée.

FALSE
  
> Les valeurs de propriété ne répondent pas à la relation spécifiée.

## <a name="remarks"></a>Remarques

La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de [propriétéSPropValue](spropvalue.md) . Les **fonctions FPropCompareProp** et [FPropContainsProp](fpropcontainsprop.md) peuvent être utilisées pour préparer les restrictions de génération d’une table.
  
L’ordre de comparaison _est lpSPropValue1_, _ulRelOp_, _lpSPropValue2_. Si les types de propriété des valeurs de propriété à comparer ne correspondent pas, la **fonction FPropCompareProp** renvoie false.
