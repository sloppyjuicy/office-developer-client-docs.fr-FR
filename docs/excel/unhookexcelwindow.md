---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- fonction unhookexcelwindow
ms.localizationpriority: medium
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
ms.openlocfilehash: 2f5469a54a24421ac3551901d2f95e8b5f69f3f9
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198764"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Supprime **l’ExcelCursorProc** qui a été précédemment installé par **HookExcelWindow**. Cela aurait été fait de sorte **qu’ExcelCursorProc** a été appelé avant le Microsoft Excel **principal WndProc**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Paramètres

 _hWndExcel_ (**HANDLE**)
  
Le Excel de Windows principal.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction ne retourne pas de valeur.
  
## <a name="remarks"></a>Remarques

Cette fonction restaure la Excel **WndProc** par défaut à l’aide de **SetWindowLong()** pour restaurer l’adresse enregistrée par **HookExcelWindow()**.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

