---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310247"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Permet de renvoyer le résultat d'une fonction définie par l'utilisateur (UDF) asynchrone.
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Paramètres

_pxAsyncHandle_ (**xltypeBigData**)
  
Handle asynchrone de la FDU vers laquelle le résultat est renvoyé.
  
_pxFunctionResult_
  
Valeur de retour de la FDU.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Si elle réussit, renvoie la **valeur true** (**xltypeBool**). En cas d'échec, renvoie **false**.
  
## <a name="remarks"></a>Remarques

**xlAsyncReturn** est le seul rappel qu'Excel autorise sur les threads de non calcul lors du recalcul. La partie asynchrone d'une FDU asynchrone ne doit pas effectuer de rappels autres que **xlAsyncReturn**. Le XLL doit libérer de la mémoire allouée pour conserver la valeur de retour.
  
Les paramètres _pxAsyncHandle_ et _pxFunctionResult_ peuvent également être de type **xltypeMulti** lorsqu'ils sont utilisés pour renvoyer un tableau de handles et des valeurs correspondantes dans un seul rappel. Lors de l'utilisation d'un seul rappel, transmettez un LPXLOPER12 qui pointe vers les structures XLOPER12 qui contiennent un tableau de dimensions contenant les handles asynchrones et les valeurs de retour. Ces tableaux doivent être dans le même ordre pour qu'Excel corresponde correctement à un handle asynchrone avec sa valeur correspondante. 
  
L'exemple suivant montre comment vous pouvez créer un appel en lot à l'aide de **xlAsyncReturn**.
  
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

