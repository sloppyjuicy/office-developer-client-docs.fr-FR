---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- fonction xludf [excel 2007]
ms.localizationpriority: medium
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
ms.openlocfilehash: 6d529b97e3e5f016986d89bf008c478fecbcb443
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199037"
---
# <a name="xludf"></a>xlUDF

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction définie par l’utilisateur (UDF). Cette fonction permet à une DLL d’appeler des fonctions Visual Basic pour Applications (VBA) définies par l’utilisateur, des fonctions de langage de macro XLM et des fonctions inscrites contenues dans d’autres macros.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Paramètres

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)
  
Référence de la fonction que vous souhaitez appeler. Il peut s’agit d’une référence de cellule de feuille macro, du nom enregistré de la fonction en tant que chaîne ou de l’ID de registre de la fonction. Pour les fonctions de add-in XLL enregistrées à l’aide de **xlfRegister** ou **REGISTER** avec l’argument  _pxFunctionText_ fourni, l’ID peut être obtenu à l’aide de **xlfEvaluate** pour rechercher le nom. 
  
_pxArg1, ..._
  
Zéro ou plusieurs arguments de la fonction définie par l’utilisateur. Lorsque vous appelez cette fonction dans les versions antérieures à Excel 2007, le nombre maximal d’arguments supplémentaires qui peuvent être passés est 29, soit 30, _pxFnRef_ compris. À compter Excel 2007, cette limite est élevée à 254, soit 255, _pxFnRef compris._
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie la valeur renvoyée par la fonction définie par l’utilisateur.
  
## <a name="example"></a>Exemple

L’exemple suivant exécute **TestMacro** dans la feuille Macro1 BOOK1.XLS. Assurez-vous que la macro se trouve sur une feuille nommée Macro1. 
  
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

