---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782240"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le descripteur d’instances de l’instance de Microsoft Excel en appelant une DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction ne comporte aucun argument.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Le descripteur d’instances (**xltypeBigData**) est inclus dans le champ **val.bigdata.h.hdata** . 
  
## <a name="remarks"></a>Remarques

Cette fonction peut être utilisée pour faire la distinction entre plusieurs instances en cours d’exécution de Microsoft Excel qui appellent la DLL.
  
Cette fonction renvoie une valeur correcte avec les versions 32 bits et 64 bits de Microsoft Excel. Elle a été introduite dans Excel 2010 comme une extension à la fonction [xlGetInst](xlgetinst.md) , qui fonctionne uniquement avec les versions 32 bits de Microsoft Excel. 
  
Cette fonction fonctionne correctement lorsqu’elle est appelée à l’aide de ces deux types de fonctions de rappel API, [Excel4 et Excel12](excel4-excel12.md) car **XLOPER** et **XLOPER12** ont la même structure qui prend en charge la valeur **xltypeBigData** tapez. 
  
## <a name="example"></a>Exemple

L’exemple suivant compare l’instance de la dernière copie d’Excel qui l’a appelé à la copie active de Microsoft Excel qui l’a appelé. Si elles sont les mêmes, elle renvoie la valeur 1 ; dans le cas contraire, elle renvoie la valeur 0 ; Si la fonction échoue, elle renvoie -1. Cet exemple fonctionne avec les versions 32 bits et 64 bits de Microsoft Excel.
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>Voir aussi

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

