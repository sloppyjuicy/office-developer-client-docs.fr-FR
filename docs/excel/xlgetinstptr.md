---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405281"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le handle d’instance de l’instance de Microsoft Excel qui appelle actuellement une DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas d’arguments.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Le handle d’instance (**xltypeBigData**) sera dans le champ **val.bigdata.h.hdata.** 
  
## <a name="remarks"></a>Remarques

Cette fonction peut être utilisée pour faire la distinction entre plusieurs instances d’Excel en cours d’exécution qui appellent la DLL.
  
Cette fonction renvoie une valeur correcte avec les versions 32 bits et 64 bits d’Excel. Il a été introduit dans Excel 2010 en tant qu’extension de la fonction [xlGetInst,](xlgetinst.md) qui fonctionne correctement uniquement avec les versions 32 bits d’Excel. 
  
Cette fonction fonctionne correctement lorsqu’elle est appelée à l’aide des variétés Excel4 et [Excel12](excel4-excel12.md) des fonctions de rappel d’API, car **XLOPER** et **XLOPER12** ont la même structure qui prend en charge le type de valeur **xltypeBigData.** 
  
## <a name="example"></a>Exemple

L’exemple suivant compare l’instance de la dernière copie d’Excel qui l’a appelée à la copie actuelle d’Excel qui l’a appelée. Si elles sont identiques, elle renvoie 1 ; si ce n’est pas le cas, elle renvoie 0 ; Si la fonction échoue, elle renvoie -1. Cet exemple fonctionne avec les versions 32 bits et 64 bits d’Excel.
  
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
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

