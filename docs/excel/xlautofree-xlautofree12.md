---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- fonction xlautofree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413289"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="f86f0-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="f86f0-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="f86f0-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f86f0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f86f0-106">Appelé par Microsoft Excel juste après qu’une fonction de feuille de calcul XLL lui renvoie une **xlOPER** /  **XLOPER12** avec un indicateur qui lui indique qu’il existe de la mémoire que le XLL doit encore libérer.</span><span class="sxs-lookup"><span data-stu-id="f86f0-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="f86f0-107">Le XLL peut ainsi renvoyer des matrices, des chaînes et des références externes allouées dynamiquement vers la feuille de calcul sans pertes de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f86f0-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="f86f0-108">Pour plus d’informations, reportez-vous à la rubrique [Gestion de la mémoire dans Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="f86f0-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="f86f0-109">À compter d’Excel 2007, la fonction **xlAutoFree12** et le type de données **XLOPER12** sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f86f0-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="f86f0-110">Excel ne nécessite pas de XLL pour implémenter et exporter l’une de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="f86f0-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="f86f0-111">Toutefois, vous devez le faire si vos fonctions XLL retournent une XLOPER ou XLOPER12 qui a été allouée dynamiquement ou qui contient des pointeurs vers la mémoire allouée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="f86f0-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="f86f0-112">Assurez-vous que votre choix de gestion de la mémoire pour ces types est cohérent dans l’ensemble de votre XLL et avec la façon dont vous avez implémenté **xlAutoFree** et **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="f86f0-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="f86f0-113">À l’intérieur de la fonction **xlAutoFree** /  **xlAutoFree12,** les rappels dans Excel sont désactivés, à une exception près : **xlFree** peut être appelé pour libérer de la mémoire allouée par Excel.</span><span class="sxs-lookup"><span data-stu-id="f86f0-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="f86f0-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f86f0-114">Parameters</span></span>

 <span data-ttu-id="f86f0-115">_pxFree_ (**LPXLOPER dans le cas de xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="f86f0-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="f86f0-116">_pxFree_ (**LPXLOPER12 dans le cas de xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="f86f0-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="f86f0-117">Pointeur vers **xlOPER** ou **XLOPER12** dont la mémoire doit être libérée.</span><span class="sxs-lookup"><span data-stu-id="f86f0-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f86f0-118">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="f86f0-118">Property value/Return value</span></span>

<span data-ttu-id="f86f0-119">Cette fonction ne retourne pas de valeur et doit être déclarée comme renvoyant void.</span><span class="sxs-lookup"><span data-stu-id="f86f0-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f86f0-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f86f0-120">Remarks</span></span>

<span data-ttu-id="f86f0-121">Lorsqu’Excel est configuré pour utiliser le recalcul de workbook multithread, **xlAutoFree** /  **xlAutoFree12** est appelé sur le thread utilisé pour appeler la fonction qui l’a renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f86f0-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="f86f0-122">L’appel à **xlAutoFree**/ **xlAutoFree12** est toujours effectué avant que d’autres cellules de la feuille de calcul soient évaluées sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="f86f0-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="f86f0-123">Cela simplifie la conception thread-safe dans votre XLL.</span><span class="sxs-lookup"><span data-stu-id="f86f0-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="f86f0-124">Si la fonction **xlAutoFree** /  **xlAutoFree12** que vous fournissez examine le champ **xltype** _de pxFree_, n’oubliez pas que le bit **xlbitDLLFree** sera toujours définie.</span><span class="sxs-lookup"><span data-stu-id="f86f0-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f86f0-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="f86f0-125">Example</span></span>

 <span data-ttu-id="f86f0-126">**Exemple d’implémentation 1**</span><span class="sxs-lookup"><span data-stu-id="f86f0-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="f86f0-127">Le premier code de l’exemple illustre une implémentation très spécifique de  `\SAMPLES\EXAMPLE\EXAMPLE.C` **xlAutoFree**, qui est conçu pour fonctionner avec une seule **fonction, fArray**.</span><span class="sxs-lookup"><span data-stu-id="f86f0-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="f86f0-128">En règle générale, votre XLL aura plusieurs fonctions qui retournent de la mémoire qui doit être libérée, auquel cas une implémentation moins restreinte est requise.</span><span class="sxs-lookup"><span data-stu-id="f86f0-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="f86f0-129">**Exemple d’implémentation 2**</span><span class="sxs-lookup"><span data-stu-id="f86f0-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="f86f0-130">Le deuxième exemple d’implémentation est cohérent avec les hypothèses utilisées dans les exemples de création **XLOPER12** de la section 1.6.3, xl12_Str_example, xl12_Ref_example et xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="f86f0-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="f86f0-131">Les hypothèses sont que, lorsque le bit **xlbitDLLFree** a été définie, toute la chaîne, le tableau et la mémoire de référence externe ont été alloués dynamiquement à l’aide de **malloc** et doivent donc être libérés dans un appel à la libération.</span><span class="sxs-lookup"><span data-stu-id="f86f0-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="f86f0-132">**Exemple d’implémentation 3**</span><span class="sxs-lookup"><span data-stu-id="f86f0-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="f86f0-133">Le troisième exemple d’implémentation est cohérent avec une XLL dans laquelle les fonctions exportées qui retournent **xlOPER12** allouent des chaînes, des références externes et des tableaux à l’aide de **malloc**, et où **xlOPER12** lui-même est également alloué dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="f86f0-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12** s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="f86f0-134">Le renvoi d’un pointeur vers une **XLOPER12** allouée dynamiquement est un moyen de s’assurer que la fonction est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f86f0-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a><span data-ttu-id="f86f0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f86f0-135">See also</span></span>



[<span data-ttu-id="f86f0-136">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="f86f0-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

