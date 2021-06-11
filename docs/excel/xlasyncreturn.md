---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414108"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour renvoyer le résultat d’une fonction asynchrone définie par l’utilisateur (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameters

_pxAsyncHandle_ (**xltypeBigData**)
  
Handle asynchrone de l’UDF à laquelle le résultat est renvoyé.
  
_pxFunctionResult_
  
Valeur de retour de l’UDF.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, renvoie **TRUE** (**xltypeBool**). En cas d’échec, renvoie **FALSE**.
  
## <a name="remarks"></a>Remarques

**xlAsyncReturn** est le seul rappel Excel threads non de calcul lors du recalcul. La partie asynchrone d’une UDF asynchrone ne doit effectuer aucun rappel autre que **xlAsyncReturn**. Le XLL doit libérer de la mémoire allouée pour contenir la valeur de retour.
  
Les paramètres _pxAsyncHandle_ et  _pxFunctionResult_ peuvent également être de type **xltypeMulti** lorsqu’ils sont utilisés pour renvoyer un tableau de handles et de valeurs correspondantes dans un rappel unique. Lorsque vous utilisez un rappel unique, passez un LPXLOPER12 qui pointe vers des structures XLOPER12 qui contiennent des tableaux à une dimension qui contiennent les poignées asynchrones et les valeurs de retour. Ces tableaux doivent être dans le même ordre pour que les Excel correspondent correctement à un handle asynchrone avec sa valeur correspondante. 
  
L’exemple suivant montre comment effectuer un appel par lots à l’aide **de xlAsyncReturn**.
  
```cpp
int batchSize = 10;
    LPXLOPER12 pHandles = new XLOPER12[batchSize];
    LPXLOPER12 pValues = new XLOPER12[batchSize];
    /*Add code to fill in LPXLOPER12 arrays (pHandles and pValues)
    with the XOPER12 structures that contain the asynchronous handles
    and values, in respective order*/
    //Create an XLOPER12 of type xltypeMulti, and fill the Handle array
    XLOPER12 handleArray;
    handleArray.xltype = xltypeMulti;
    handleArray.val.array.rows = 1;
    handleArray.val.array.columns = (COL)batchSize;
    handleArray.val.array.lparray = pHandles;
    
    //Create an XLOPER12 if type xltypeMulti, and fill the Values array
    XLOPER12 valueArray;
    valueArray.xltype = xltypeMulti;
    valueArray.val.array.rows = 1;
    valueArray.val.array.columns = (COL)batchSize;
    valueArray.val.array.lparray = pValues;
    //Make the callback with the return value
    int ret = Excel12(xlAsyncReturn, 0, 2, &amp;handleArray, &amp;valueArray);
    //Add code to free the allocated memory here (pHandles, pValues, valueArray, handleArray)
    return ret;

```

## <a name="see-also"></a>Voir aussi

- [Fonctions asynchrones définies par l’utilisateur](asynchronous-user-defined-functions.md)

