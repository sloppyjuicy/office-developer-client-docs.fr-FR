---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- fonction xlAutoFree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782213"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="67346-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="67346-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="67346-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67346-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="67346-106">Appelée par Microsoft Excel juste après qu’une fonction de feuille de calcul XLL renvoie un **XLOPER**/ **XLOPER12** lui avec un indicateur indiquant en mémoire que la XLL doit toujours libérer.</span><span class="sxs-lookup"><span data-stu-id="67346-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="67346-107">Cela permet à la ressource XLL à renvoyer allouées dynamiquement des tableaux, des chaînes et des références externes de la feuille de calcul sans fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="67346-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="67346-108">Pour plus d�informations, voir [Gestion de la m�moire dans Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="67346-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="67346-109">À compter d’Excel 2007, la fonction **xlAutoFree12** et le type de données **XLOPER12** sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="67346-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="67346-110">Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter une de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="67346-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="67346-111">Toutefois, vous devez faire si vos fonctions XLL renvoient XLOPER ou XLOPER12 qui a été affectée dynamiquement ou qui contient des pointeurs vers la mémoire allouée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="67346-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="67346-112">Assurez-vous que votre choix de la gestion de la mémoire pour ces types est cohérent au sein de votre XLL et comment vous avez implémenté **xlAutoFree** et **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="67346-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="67346-113">À l’intérieur du **xlAutoFree**/ **xlAutoFree12** fonction, des rappels dans Excel sont désactivées, à une seule exception : **xlFree** peut être appelée pour libérer de la mémoire allouée par Excel.</span><span class="sxs-lookup"><span data-stu-id="67346-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="67346-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67346-114">Parameters</span></span>

 <span data-ttu-id="67346-115">_pxFree_ (**LPXLOPER dans le cas de xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="67346-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="67346-116">_pxFree_ (**LPXLOPER12 dans le cas xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="67346-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="67346-117">Pointeur vers le **XLOPER** ou le **XLOPER12** disposant de mémoire qui doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="67346-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="67346-118">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="67346-118">Property value/Return value</span></span>

<span data-ttu-id="67346-119">Cette fonction ne retourne pas de valeur et doit être déclarée comme renvoyant des valeurs nulles.</span><span class="sxs-lookup"><span data-stu-id="67346-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67346-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="67346-120">Remarks</span></span>

<span data-ttu-id="67346-121">Lorsque Excel est configuré pour utiliser le recalcul de classeurs multithread, **xlAutoFree**/ **xlAutoFree12** est appelée sur le même thread utilisé pour appeler la fonction qui a renvoyé.</span><span class="sxs-lookup"><span data-stu-id="67346-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="67346-122">L’appel à **xlAutoFree**/ **xlAutoFree12** est toujours effectuées avant l’évaluation des cellules de la feuille de calcul suivantes sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="67346-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="67346-123">Cela simplifie la création de thread-safe dans votre XLL.</span><span class="sxs-lookup"><span data-stu-id="67346-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="67346-124">Si le **xlAutoFree**/ **xlAutoFree12** fonction que vous indiquez examine le champ **xltype** de _pxFree_, n’oubliez pas que le bit **xlbitDLLFree** est toujours défini.</span><span class="sxs-lookup"><span data-stu-id="67346-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="67346-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="67346-125">Example</span></span>

 <span data-ttu-id="67346-126">**Implémentation de l’exemple 1**</span><span class="sxs-lookup"><span data-stu-id="67346-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="67346-127">Le code du premier `\SAMPLES\EXAMPLE\EXAMPLE.C` illustre une implémentation très spécifique de **xlAutoFree**, qui est conçu pour fonctionner avec une fonction, **fArray**.</span><span class="sxs-lookup"><span data-stu-id="67346-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="67346-128">En règle générale, votre XLL ont plusieurs fonction retourner la mémoire qui doit être libéré, auquel cas une implémentation moins restrictives est requise.</span><span class="sxs-lookup"><span data-stu-id="67346-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="67346-129">**Implémentation de l’exemple 2**</span><span class="sxs-lookup"><span data-stu-id="67346-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="67346-130">Le deuxième exemple d’implémentation est cohérent avec les hypothèses utilisées dans les exemples de création **XLOPER12** dans la section 1.6.3, xl12_Str_example, xl12_Ref_example et xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="67346-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="67346-131">Les hypothèses sont qui, lorsque le bit **xlbitDLLFree** a été set, tous les string, array, mémoire référence externe a été affectée dynamiquement à l’aide de **malloc**et doit donc être libéré dans un appel pour libérer de le.</span><span class="sxs-lookup"><span data-stu-id="67346-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="67346-132">**Exemple d’implémentation 3**</span><span class="sxs-lookup"><span data-stu-id="67346-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="67346-133">Le troisième exemple d’implémentation est cohérent avec une solution XLL où exporté des fonctions qui retournent **XLOPER12**s allouent des chaînes, les références externes et les tableaux à l’aide de **malloc**et le **XLOPER12** proprement dite est également affectés dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="67346-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12**s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="67346-134">Renvoi d’un pointeur vers alloué dynamiquement **XLOPER12** est pour vous assurer que la fonction est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="67346-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="67346-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67346-135">See also</span></span>



[<span data-ttu-id="67346-136">Gestionnaire de compléments et les fonctions de l’Interface XLL</span><span class="sxs-lookup"><span data-stu-id="67346-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

