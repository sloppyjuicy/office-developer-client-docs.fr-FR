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
ms.localizationpriority: medium
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
ms.openlocfilehash: 4566fa6c875f37854cdc0737b2e9b71d53fe5b69
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198159"
---
# <a name="xlsheetid"></a>xlSheetId

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Recherche l’ID de feuille d’une feuille nommée afin de construire des références externes.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Paramètres

_pxSheetName_ (**xltypeStr**)
  
(Facultatif). Nom du livre et de la feuille que vous souhaitez connaître. Si elle est omise, **la fonction xlSheetId** renvoie l’ID de feuille de la feuille active (avant). 
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie l’ID de feuille  _dans pxRes- \> val.mref.idSheet_. 
  
> [!NOTE]
> Le pointeur du tableau  _pxRes- \> val.mref.lpmref_ est définie sur NULL après cet appel, de sorte qu’il n’est pas nécessaire d’appeler **xlFree** pour libérer la mémoire que ce type contient normalement, bien qu’il soit totalement sûr de le faire. 
  
## <a name="remarks"></a>Remarques

Le workbook contenant la feuille spécifiée doit être ouvert pour utiliser cette fonction. Il n’existe aucun moyen de construire une référence à un livre de travail non ouvert à partir d’une DLL. Pour plus d’informations sur l’utilisation de **xlSheetId** pour construire des références, voir Gestion de [la mémoire dans Excel](memory-management-in-excel.md) pour obtenir des exemples de construction **xltypeRef.** 
  
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

