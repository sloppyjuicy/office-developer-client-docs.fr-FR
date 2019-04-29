---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- fonction xlSheetNm [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437412"
---
# <a name="xlsheetnm"></a>xlSheetNm

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Renvoie le nom d'une feuille de calcul ou d'une feuille macro à partir de son ID de feuille interne contenu dans une référence externe ou du nom de la feuille active si une référence interne lui a été transmise.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Paramètres

_pxExtref_ (**xltypeRef** ou **xltypeSRef**)
  
Référence à la feuille dont vous souhaitez obtenir le nom.
  
Si vous transférez une référence externe (**xltypeRef**), elle doit uniquement contenir l'ID de la feuille. Les structures de données qui décrivent les cellules de la feuille de calcul sont ignorées et n'ont pas besoin d'être fournies. Si la valeur de l'ID est définie sur zéro, **xlSheetNm** renvoie le nom de la feuille actuelle. 
  
Si vous transférez une référence interne (**xltypeSef**), **xlSheetNm** renvoie le nom de la feuille actuelle. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie le nom de la feuille (**xltypeStr**) dans le formulaire `[Book1]Sheet1`.
  
## <a name="example"></a>Exemple

L'exemple suivant montre comment afficher le nom de la feuille à partir de laquelle la fonction a été appelée. La fonction fonctionne correctement uniquement si elle est appelée à partir d'une feuille macro lors de l'exécution d'une macro de commande XLM. Cela est dû au fait qu'il appelle **xlcAlert**, que seules les commandes peuvent faire, et qu'il doit être appelé à partir d'une feuille plutôt que d'une boîte de dialogue, d'un menu ou d'une barre de commandes afin que **xlfCaller** renvoie une référence. 
  
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
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

