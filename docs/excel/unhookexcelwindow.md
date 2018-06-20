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
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782205"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Supprime **ExcelCursorProc** qui a été précédemment installé par **HookExcelWindow**. Cette tâche ont effectue afin que **ExcelCursorProc** a été appelé avant **WndProc**Microsoft Excel principale.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Paramètres

 _hWndExcel_ (**Gérer**)
  
La fenêtre principale Excel gère.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

La fonction ne retourne pas une valeur.
  
## <a name="remarks"></a>Remarques

Cette fonction restaure la valeur par défaut Excel **WndProc** pour restaurer l’adresse qui a été enregistré par **HookExcelWindow()** à l’aide de **SetWindowLong()** .
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

