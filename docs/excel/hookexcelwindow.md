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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782137"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Installe **ExcelCursorProc** afin qu’elle est appelée avant **WndProc**Microsoft Excel principale.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Paramètres

 _hWndExcel_ (**Gérer**)
  
La fenêtre principale Excel gère.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

La fonction ne retourne pas une valeur.
  
## <a name="remarks"></a>Remarques

La fonction obtient l’adresse d' Excel **WndProc** **GetWindowLong()** grâce à l’utilisation. Il stocke cette valeur dans global qui peut être utilisée pour appeler la valeur par défaut **WndProc** et également pour la restaurer. Enfin, il remplace cette adresse avec l’adresse **ExcelCursorProc** à l’aide de **SetWindowLong()**.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

