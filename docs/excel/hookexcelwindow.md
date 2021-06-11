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
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413506"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Installe **ExcelCursorProc** afin qu’il soit appelé avant le Microsoft Excel **principal WndProc**.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameters

 _hWndExcel_ (**HANDLE**)
  
Le Excel de Windows principal.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction ne retourne pas de valeur.
  
## <a name="remarks"></a>Remarques

La fonction obtient l’adresse du Excel **WndProc** via l’utilisation de **GetWindowLong()**. Elle stocke cette valeur dans un global qui peut être utilisé pour appeler le **WndProc** par défaut et également pour la restaurer. Enfin, elle remplace cette adresse par l’adresse **d’ExcelCursorProc** à l’aide **de SetWindowLong()**.
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

