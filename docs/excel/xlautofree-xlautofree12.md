---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- fonction xlAutoFree [Excel 2007]
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
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Appelé par Microsoft Excel juste après qu'une fonction de feuille de calcul XLL renvoie un élément **XLOPER**/ **** , avec un indicateur qui indique qu'il existe une mémoire que la XLL doit encore libérer. Le XLL peut ainsi renvoyer des matrices, des chaînes et des références externes allouées dynamiquement vers la feuille de calcul sans pertes de mémoire. Pour plus d’informations, reportez-vous à la rubrique [Gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
À partir d'Excel 2007, la fonction **xlAutoFree12** et le type de données **XLOPER12** sont pris en charge. 
  
Excel ne nécessite pas de XLL pour implémenter et exporter l'une ou l'autre de ces fonctions. Toutefois, vous devez le faire si vos fonctions XLL renvoient un XLOPER ou un XLOPER12 qui a été alloué dynamiquement ou qui contient des pointeurs vers la mémoire allouée dynamiquement. Assurez-vous que votre choix concernant la gestion de la mémoire pour ces types est cohérent dans l'ensemble de votre XLL et sur la façon dont vous avez implémenté **xlAutoFree** et **xlAutoFree12**.
  
À l'intérieur de la fonction**xlAutoFree12** **xlAutoFree**/ , les rappels dans Excel sont désactivés, à une exception près: **xlFree** peut être appelé pour libérer de la mémoire allouée par Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Paramètres

 _pxFree_ (**LPXLOPER dans le cas de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 dans le cas de xlAutoFree12**)
  
Pointeur vers l' **XLOPER** ou le **XLOPER12** dont la mémoire doit être libérée. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Cette fonction ne renvoie pas de valeur et doit être déclarée comme renvoyant void.
  
## <a name="remarks"></a>Remarques

Lorsque Excel est configuré pour utiliser le recalcul de classeurs multithread, **xlAutoFree**/ **xlAutoFree12** est appelé sur le même thread que celui utilisé pour appeler la fonction qui l'a retourné. L’appel à **xlAutoFree**/ **xlAutoFree12** est toujours effectué avant que d’autres cellules de la feuille de calcul soient évaluées sur ce thread. Cela simplifie la conception thread-safe dans votre XLL. 
  
Si la fonction **xlAutoFree**/ **xlAutoFree12** que vous fournissez examine le champ **xltype** de _pxFree_, n'oubliez pas que le bit **xlbitDLLFree** sera toujours défini. 
  
## <a name="example"></a>Exemple

 **Exemple d'implémentation 1**
  
Le premier code de `\SAMPLES\EXAMPLE\EXAMPLE.C` montre une implémentation très spécifique de **xlAutoFree**, qui est conçue pour fonctionner avec une seule fonction, **fArray**. En règle générale, votre XLL dispose de plusieurs fonctions de retour de mémoire qui doivent être libérées, auquel cas une implémentation moins restreinte est requise. 
  
 **Exemple d'implémentation 2**
  
Le deuxième exemple d'implémentation est conforme aux hypothèses utilisées dans les exemples de création de **XLOPER12** de la section 1.6.3, Xl12_Str_example, Xl12_Ref_example et xl12_Multi_example. Les hypothèses sont que, lorsque le bit **xlbitDLLFree** a été défini, tous les caractères de la chaîne, de la matrice et de la mémoire de référence externe ont été alloués dynamiquement à l'aide de **malloc**, et donc doivent être libérés dans un appel à Free.
  
 **Exemple d'implémentation 3**
  
Le troisième exemple de mise en œuvre est cohérent avec un XLL où des fonctions exportées renvoient des objets **XLOPER12**, des références externes et des tableaux à l'aide de **malloc**, et où le **XLOPER12** lui-même est également alloué dynamiquement. Le renvoi d'un pointeur à une méthode **XLOPER12** allouée dynamiquement est une façon de s'assurer que la fonction est thread-safe. 
  
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

