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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564604"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété à l’aide d’un opérateur relationnel spécifié. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Paramètres

_lpSPropValue1_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définition de la première valeur de propriété pour la comparaison. 
    
_ulRelOp_
  
> [in] L’opérateur relationnel à utiliser dans la comparaison. Pour les valeurs possibles, voir la structure [SComparePropsRestriction](scomparepropsrestriction.md) . 
    
_lpSPropValue2_
  
> [in] Pointeur vers une structure **SPropValue** définissant la valeur de la propriété deuxième pour la comparaison. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Les valeurs de propriété satisfont à l’objet relation spécifié. 
    
FALSE 
  
> Les valeurs de propriété ne répondent pas à l’objet relation spécifié.
    
## <a name="remarks"></a>Remarques

Les types de propriétés spécifiés dans les définitions de propriétés [SPropValue](spropvalue.md) dépend de la méthode de comparaison. Les fonctions **FPropCompareProp** et [FPropContainsProp](fpropcontainsprop.md) peuvent servir à préparer des restrictions pour la génération d’une table. 
  
L’ordre de comparaison est _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Si les valeurs de propriété à comparer les types de propriétés ne correspondent pas, la fonction **FPropCompareProp** renvoie la valeur FALSE. 
  

