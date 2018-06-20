---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e7ba37629ff2198339394448410ffd16477d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782209"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour renvoyer le résultat d’une fonction définie par l’utilisateur (UDF) asynchrone.
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Paramètres

_pxAsyncHandle_ (**xltypeBigData**)
  
Handle asynchrone de l’UDF à laquelle le résultat est retourné.
  
_pxFunctionResult_
  
La valeur de retour de l’UDF.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Si l’opération réussit, renvoie **la valeur TRUE** (**xltypeBool**). En cas d’échec, renvoie **FALSE**.
  
## <a name="remarks"></a>Remarques

**xlAsyncReturn** est le rappel uniquement que permet d’Excel sur des threads non calcul pendant le recalcul. La partie d’une fichier UDF asynchrone asynchrone n’effectuez des rappels autre que **xlAsyncReturn**. La ressource XLL doit libérer de la mémoire allouée pour contenir la valeur de retour.
  
Les paramètres _pxAsyncHandle_ et _pxFunctionResult_ peuvent également être de type **xltypeMulti** lorsqu’elle est utilisée pour retourner un tableau de handles et les valeurs correspondantes dans un rappel unique. Lorsque vous utilisez un seul rappel, passez un LPXLOPER12 qui pointe vers les structures XLOPER12 qui contiennent un tableaux multidimensionnels qui contiennent les poignées asynchrones et valeurs de retour. Ces tableaux doivent être dans le même ordre pour Excel correctement correspondre une poignée asynchrone avec sa valeur correspondante. 
  
L’exemple suivant montre comment vous pouvez faire appel à l’aide de **xlAsyncReturn**un lot.
  
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

