---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- fonction UnhookExcelWindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409446"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Supprime le **ExcelCursorProc** qui a été précédemment installé par **HookExcelWindow**. Cette opération aurait été réalisée de sorte que **ExcelCursorProc** ait été appelé avant Microsoft Excel principal **WndProc**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Paramètres

 _hWndExcel_ (**Handle**)
  
Le descripteur Windows principal d'Excel.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction ne renvoie pas de valeur.
  
## <a name="remarks"></a>Remarques

Cette fonction restaure la valeur par défaut **** d'Excel à l'aide de **SetWindowLong ()** pour restaurer l'adresse enregistrée par **HookExcelWindow ()**.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

