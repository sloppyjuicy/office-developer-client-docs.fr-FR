---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- fonction xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782235"
---
# <a name="xlsheetid"></a>xlSheetId

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Recherche de l’ID de feuille d’une feuille nommée afin de construire des références externes.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Paramètres

_pxSheetName_ (**xltypeStr**)
  
(Facultatif). Le nom de l’annuaire et de la feuille que vous souhaitez découvrir. Si tous deux omis, la fonction **xlSheetId** renvoie l’ID de feuille de la feuille active (avant). 
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie l’ID de feuille de _pxRes -\>val.mref.idSheet_. 
  
> [!NOTE]
> La _pxRes -\>val.mref.lpmref_ pointeur de tableau a la valeur NULL après cet appel afin qu’il n’est pas nécessaire d’appeler **xlFree** pour libérer de la mémoire contenant ce type normalement, bien qu’il soit entièrement fiable à le faire. 
  
## <a name="remarks"></a>Remarques

Le classeur contenant la feuille spécifiée doit être ouvert pour utiliser cette fonction. Il n’existe aucun moyen pour construire une référence à un classeur non ouvert à partir d’une DLL. Pour plus d’informations sur l’utilisation de **xlSheetId** pour construire les références, voir [Gestion de la mémoire dans Excel](memory-management-in-excel.md) pour obtenir des exemples de construction **xltypeRef** . 
  
## <a name="example"></a>Exemple

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi

- [xlSheetNm](xlsheetnm.md)
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

