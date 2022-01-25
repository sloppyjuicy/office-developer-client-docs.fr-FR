---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- fonction hookexcelwindow [excel 2007]
ms.localizationpriority: medium
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
ms.openlocfilehash: 34f57a5c8c3eb9b81e2874ae050148831c5fda8b
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199576"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Installe **ExcelCursorProc** afin qu’il soit appelé avant le Microsoft Excel **principal WndProc**.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Paramètres

 _hWndExcel_ (**HANDLE**)
  
Le Excel de Windows principal.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction ne retourne pas de valeur.
  
## <a name="remarks"></a>Remarques

La fonction obtient l’adresse du Excel **WndProc** via l’utilisation de **GetWindowLong()**. Elle stocke cette valeur dans un global qui peut être utilisé pour appeler le **WndProc** par défaut et également pour la restaurer. Enfin, elle remplace cette adresse par l’adresse **d’ExcelCursorProc** à l’aide **de SetWindowLong()**.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

