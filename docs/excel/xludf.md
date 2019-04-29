---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- fonction xlUDF [Excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430643"
---
# <a name="xludf"></a>xlUDF

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction définie par l'utilisateur (UDF). Cette fonction permet à une DLL d'appeler des fonctions définies par l'utilisateur Visual Basic pour applications (VBA), des fonctions de langage de macro XLM et des fonctions inscrites contenues dans d'autres compléments.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Paramètres

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)
  
Référence de la fonction que vous souhaitez appeler. Il peut s'agir d'une référence de cellule de feuille macro, du nom enregistré de la fonction sous forme de chaîne ou de l'ID de la fonction. Pour les fonctions de complément XLL inscrites à l'aide de **xlfRegister** ou **s'inscrire** avec l'argument _pxFunctionText_ fourni, l'ID peut être obtenu à l'aide de **xlfEvaluate** pour rechercher le nom. 
  
_pxArg1,..._
  
Zéro ou plusieurs arguments de la fonction définie par l'utilisateur. Lorsque vous appelez cette fonction dans les versions antérieures à Excel 2007, le nombre maximal d'arguments supplémentaires qui peuvent être passés est 29, soit 30, y compris _pxFnRef_. À partir d'Excel 2007, cette limite est augmentée à 254, soit 255 y compris _pxFnRef_.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie la valeur renvoyée par la fonction définie par l'utilisateur.
  
## <a name="example"></a>Exemple

L'exemple suivant exécute **TestMacro** sur la feuille Macro1 dans le classeur BOOK1. XLS. Assurez-vous que la macro se trouve sur une feuille nommée Macro1. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi

- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

