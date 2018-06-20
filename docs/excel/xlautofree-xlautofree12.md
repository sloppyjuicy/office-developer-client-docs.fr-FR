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
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelée par Microsoft Excel juste après qu’une fonction de feuille de calcul XLL renvoie un **XLOPER**/ **XLOPER12** lui avec un indicateur indiquant en mémoire que la XLL doit toujours libérer. Cela permet à la ressource XLL à renvoyer allouées dynamiquement des tableaux, des chaînes et des références externes de la feuille de calcul sans fuites de mémoire. Pour plus d�informations, voir [Gestion de la m�moire dans Excel](memory-management-in-excel.md).
  
À compter d’Excel 2007, la fonction **xlAutoFree12** et le type de données **XLOPER12** sont pris en charge. 
  
Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter une de ces fonctions. Toutefois, vous devez faire si vos fonctions XLL renvoient XLOPER ou XLOPER12 qui a été affectée dynamiquement ou qui contient des pointeurs vers la mémoire allouée dynamiquement. Assurez-vous que votre choix de la gestion de la mémoire pour ces types est cohérent au sein de votre XLL et comment vous avez implémenté **xlAutoFree** et **xlAutoFree12**.
  
À l’intérieur du **xlAutoFree**/ **xlAutoFree12** fonction, des rappels dans Excel sont désactivées, à une seule exception : **xlFree** peut être appelée pour libérer de la mémoire allouée par Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Paramètres

 _pxFree_ (**LPXLOPER dans le cas de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 dans le cas xlAutoFree12**)
  
Pointeur vers le **XLOPER** ou le **XLOPER12** disposant de mémoire qui doit être libéré. 
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Cette fonction ne retourne pas de valeur et doit être déclarée comme renvoyant des valeurs nulles.
  
## <a name="remarks"></a>Remarques

Lorsque Excel est configuré pour utiliser le recalcul de classeurs multithread, **xlAutoFree**/ **xlAutoFree12** est appelée sur le même thread utilisé pour appeler la fonction qui a renvoyé. L’appel à **xlAutoFree**/ **xlAutoFree12** est toujours effectuées avant l’évaluation des cellules de la feuille de calcul suivantes sur ce thread. Cela simplifie la création de thread-safe dans votre XLL. 
  
Si le **xlAutoFree**/ **xlAutoFree12** fonction que vous indiquez examine le champ **xltype** de _pxFree_, n’oubliez pas que le bit **xlbitDLLFree** est toujours défini. 
  
## <a name="example"></a>Exemple

 **Implémentation de l’exemple 1**
  
Le code du premier `\SAMPLES\EXAMPLE\EXAMPLE.C` illustre une implémentation très spécifique de **xlAutoFree**, qui est conçu pour fonctionner avec une fonction, **fArray**. En règle générale, votre XLL ont plusieurs fonction retourner la mémoire qui doit être libéré, auquel cas une implémentation moins restrictives est requise. 
  
 **Implémentation de l’exemple 2**
  
Le deuxième exemple d’implémentation est cohérent avec les hypothèses utilisées dans les exemples de création **XLOPER12** dans la section 1.6.3, xl12_Str_example, xl12_Ref_example et xl12_Multi_example. Les hypothèses sont qui, lorsque le bit **xlbitDLLFree** a été set, tous les string, array, mémoire référence externe a été affectée dynamiquement à l’aide de **malloc**et doit donc être libéré dans un appel pour libérer de le.
  
 **Exemple d’implémentation 3**
  
Le troisième exemple d’implémentation est cohérent avec une solution XLL où exporté des fonctions qui retournent **XLOPER12**s allouent des chaînes, les références externes et les tableaux à l’aide de **malloc**et le **XLOPER12** proprement dite est également affectés dynamiquement. Renvoi d’un pointeur vers alloué dynamiquement **XLOPER12** est pour vous assurer que la fonction est thread-safe. 
  
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



[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)

