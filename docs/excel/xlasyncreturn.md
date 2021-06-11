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
# <a name="xlasyncreturn"></a><span data-ttu-id="693e6-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="693e6-103">xlAsyncReturn</span></span>

<span data-ttu-id="693e6-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="693e6-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="693e6-105">Utilisé pour renvoyer le résultat d’une fonction asynchrone définie par l’utilisateur (UDF).</span><span class="sxs-lookup"><span data-stu-id="693e6-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="693e6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="693e6-106">Parameters</span></span>

<span data-ttu-id="693e6-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="693e6-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="693e6-108">Handle asynchrone de l’UDF à laquelle le résultat est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="693e6-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="693e6-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="693e6-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="693e6-110">Valeur de retour de l’UDF.</span><span class="sxs-lookup"><span data-stu-id="693e6-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="693e6-111">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="693e6-111">Property value/Return value</span></span>

<span data-ttu-id="693e6-112">Si elle réussit, renvoie **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="693e6-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="693e6-113">En cas d’échec, renvoie **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="693e6-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="693e6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="693e6-114">Remarks</span></span>

<span data-ttu-id="693e6-115">**xlAsyncReturn** est le seul rappel Excel threads non de calcul lors du recalcul.</span><span class="sxs-lookup"><span data-stu-id="693e6-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="693e6-116">La partie asynchrone d’une UDF asynchrone ne doit effectuer aucun rappel autre que **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="693e6-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="693e6-117">Le XLL doit libérer de la mémoire allouée pour contenir la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="693e6-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="693e6-118">Les paramètres _pxAsyncHandle_ et  _pxFunctionResult_ peuvent également être de type **xltypeMulti** lorsqu’ils sont utilisés pour renvoyer un tableau de handles et de valeurs correspondantes dans un rappel unique.</span><span class="sxs-lookup"><span data-stu-id="693e6-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="693e6-119">Lorsque vous utilisez un rappel unique, passez un LPXLOPER12 qui pointe vers des structures XLOPER12 qui contiennent des tableaux à une dimension qui contiennent les poignées asynchrones et les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="693e6-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="693e6-120">Ces tableaux doivent être dans le même ordre pour que les Excel correspondent correctement à un handle asynchrone avec sa valeur correspondante.</span><span class="sxs-lookup"><span data-stu-id="693e6-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="693e6-121">L’exemple suivant montre comment effectuer un appel par lots à l’aide **de xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="693e6-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="693e6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="693e6-122">See also</span></span>

- [<span data-ttu-id="693e6-123">Fonctions asynchrones définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="693e6-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

