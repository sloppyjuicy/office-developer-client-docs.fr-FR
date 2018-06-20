---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- fonction xlUDF [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782246"
---
# <a name="xludf"></a>xlUDF

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction définie par l’utilisateur (UDF). Cette fonction permet une DLL pour appeler Visual Basic pour des fonctions définies par l’utilisateur d’Applications (VBA), les fonctions de langage macro XLM et des fonctions contenues dans d’autres compléments.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Paramètres

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)
  
La référence de la fonction à appeler. Il peut s’agir d’une référence de la cellule de la feuille de macro, le nom enregistré de la fonction sous forme de chaîne ou l’identificateur de Registre de la fonction. Pour les fonctions XLL complément inscrits à l’aide de **xlfRegister** ou **enregistrez** avec l' argument _pxFunctionText_ fourni, l’ID peut être obtenu à l’aide de **xlfEvaluate** pour rechercher le nom. 
  
_pxArg1..._
  
Zéro ou plusieurs arguments à la fonction définie par l’utilisateur. Lorsque vous appelez cette fonction dans les versions antérieures à Excel 2007, le nombre maximal d’arguments supplémentaires qui peuvent être transmises est 29, 30, y compris _pxFnRef_. À compter d’Excel 2007, cette limite est déclenchée à 254, qui est 255, y compris _pxFnRef_.
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie la valeur qui la fonction définie par l’utilisateur est renvoyée.
  
## <a name="example"></a>Exemple

L’exemple suivant exécute **TestMacro** sur feuille Macro1 Classeur1. XLS. Assurez-vous que la macro est effectuée sur une feuille nommée Macro1. 
  
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

- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

