---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- fonction xlSheetId [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428430"
---
# <a name="xlsheetid"></a>xlSheetId

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Recherche l'ID de feuille d'une feuille nommée afin de construire des références externes.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Paramètres

_pxSheetName_ (**xltypeStr**)
  
(Facultatif). Nom du livre et de la feuille à rechercher. Si cet argument est omis, la fonction **xlSheetId** renvoie l'ID de feuille de la feuille (avant) active. 
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie l'ID de la feuille dans _pxRes-\>Val. mref. idSheet_. 
  
> [!NOTE]
> Le pointeur de tableau _pxRes-\>Val. mref. lpmref_ est défini sur null après cet appel de sorte qu'il n'est pas nécessaire d'appeler **xlFree** pour libérer la mémoire que ce type contient normalement, bien qu'il soit entièrement sûr de le faire. 
  
## <a name="remarks"></a>Remarques

Le classeur contenant la feuille spécifiée doit être ouvert pour utiliser cette fonction. Il n'existe aucun moyen de créer une référence à un classeur non ouvert à partir d'une DLL. Pour plus d'informations sur l'utilisation de **xlSheetId** pour construire des références, consultez la rubrique gestion de la [mémoire dans Excel](memory-management-in-excel.md) pour obtenir des exemples de construction de **xltypeRef** . 
  
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
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

