---
title: xlAutoFree/xlAutoFree12
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- fonction xlautofree [excel 2007]
ms.localizationpriority: medium
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
ms.openlocfilehash: c0993e88f84553f538d26ef38025a3fac7dbcc1d
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788639"
---
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Appelé par Microsoft Excel juste après qu’une fonction de feuille de calcul XLL lui renvoie une **xlOPERXLOPER12** /  avec un indicateur qui lui indique qu’il existe de la mémoire que le XLL doit encore libérer. Le XLL peut ainsi renvoyer des matrices, des chaînes et des références externes allouées dynamiquement vers la feuille de calcul sans pertes de mémoire. Pour plus d’informations, reportez-vous à la rubrique [Gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
À compter Excel 2007, la fonction **xlAutoFree12** et le type de données **XLOPER12** sont pris en charge.
  
Excel ne nécessite pas de XLL pour implémenter et exporter l’une de ces fonctions. Toutefois, vous devez le faire si vos fonctions XLL retournent une XLOPER ou XLOPER12 qui a été allouée dynamiquement ou qui contient des pointeurs vers la mémoire allouée dynamiquement. Assurez-vous que votre choix de gestion de la mémoire pour ces types est cohérent dans l’ensemble de votre XLL et avec la façon dont vous avez implémenté **xlAutoFree** et **xlAutoFree12**.
  
À l’intérieur de la fonction xlAutoFreexlAutoFree12, les rappels dans Excel sont désactivés, à une exception près : **xlFree**/  peut être appelé pour libérer Excel mémoire allouée. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Paramètres

 _pxFree_ (**LPXLOPER dans le cas de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 dans le cas de xlAutoFree12**)
  
Pointeur vers **xlOPER** ou **XLOPER12** dont la mémoire doit être libérée.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Cette fonction ne retourne pas de valeur et doit être déclarée comme renvoyant void.
  
## <a name="remarks"></a>Remarques

Lorsque Excel est configuré pour utiliser le recalcul de workbook multithread, **xlAutoFreexlAutoFree12** /  est appelé sur le thread utilisé pour appeler la fonction qui l’a renvoyée. L’appel à **xlAutoFree**/ **xlAutoFree12** est toujours effectué avant que d’autres cellules de la feuille de calcul soient évaluées sur ce thread. Cela simplifie la conception thread-safe dans votre XLL.
  
Si la fonction xlAutoFreexlAutoFree12 /  que vous fournissez examine le champ **xltype** _de pxFree_, n’oubliez pas que le bit **xlbitDLLFree** sera toujours définie. 
  
## <a name="example"></a>Exemple

 **Exemple d’implémentation 1**
  
Le premier code de  `\SAMPLES\EXAMPLE\EXAMPLE.C` l’exemple illustre une implémentation très spécifique de **xlAutoFree**, qui est conçue pour fonctionner avec une seule **fonction, fArray**. En règle générale, votre XLL aura plusieurs fonctions qui retournent de la mémoire qui doit être libérée, auquel cas une implémentation moins restreinte est requise.
  
 **Exemple d’implémentation 2**
  
Le deuxième exemple d’implémentation est cohérent avec les hypothèses utilisées dans les exemples de création **XLOPER12** de la section 1.6.3, xl12_Str_example, xl12_Ref_example et xl12_Multi_example. L’hypothèse est que, lorsque le bit **xlbitDLLFree** a été définie, toute la chaîne, le tableau et la mémoire de référence externe ont été alloués dynamiquement à l’aide de **malloc** et doivent donc être libérés dans un appel à la libération.
  
 **Exemple d’implémentation 3**
  
Le troisième exemple d’implémentation est cohérent avec une XLL dans laquelle les fonctions exportées qui retournent **XLOPER12** allouent des chaînes, des références externes et des tableaux à l’aide de **malloc**, et où **xlOPER12** lui-même est également alloué dynamiquement. Le renvoi d’un pointeur vers une **XLOPER12** allouée dynamiquement est un moyen de s’assurer que la fonction est thread-safe.
  
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

## <a name="see-also"></a>Voir aussi

[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)
