---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- fonction xlsheetnm [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782245"
---
# <a name="xlsheetnm"></a>xlSheetNm

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le nom d’une feuille de calcul ou une feuille macro à partir de son ID interne feuille contenue dans une référence externe, ou le nom de la feuille en cours si passé une référence interne.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Paramètres

_pxExtref_ (**xltypeRef** ou **xltypeSRef**)
  
Une référence à la feuille dont vous souhaitez que le nom.
  
Si vous passez une référence externe (**xltypeRef**) il doit contenir uniquement l’ID de la feuille. Les structures de données qui décrivent les cellules de la feuille de calcul sont ignorées et n’avez pas besoin de fournir. Si l’ID est défini sur zéro, **xlSheetNm** renvoie le nom de la feuille active. 
  
Si vous passez une référence interne (**xltypeSef**), **xlSheetNm** renvoie le nom de la feuille active. 
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Renvoie le nom de la feuille (**xltypeStr**) sous la forme `[Book1]Sheet1`.
  
## <a name="example"></a>Exemple

L’exemple suivant affiche le nom de la feuille à partir de laquelle la fonction a été appelée. La fonction fonctionne correctement uniquement si appelée à partir d’une feuille macro lors de l’exécution d’une macro de commande XLM. Il s’agit parce qu’elle appelle **xlcAlert**, laquelle uniquement les commandes peuvent faire et elle doit être appelée à partir d’une feuille plutôt qu’une boîte de dialogue, un menu ou la barre de commandes dans l’ordre pour **xlfCaller** renvoyer une référence. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi

- [xlSheetId](xlsheetid.md)
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

