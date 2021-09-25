---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5357bd8a2adc470322b772ceabbeaef8596290f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621044"
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

## <a name="parameters"></a>Paramètres

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
  

