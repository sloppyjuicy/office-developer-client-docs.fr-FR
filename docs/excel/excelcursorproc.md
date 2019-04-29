---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- fonction ExcelCursorProc [Excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432491"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Lorsqu'une boîte de dialogue modale est affichée sur la fenêtre Microsoft Excel, le curseur est occupé sur la fenêtre Excel. Cette **WndProc** intercepte les messages Windows de type WM_SETCURSOR et replace le curseur sur une flèche normale. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Paramètres

 _hWndDlg_ (**HWND**)
  
Contient le handle Windows HWND de la boîte de dialogue.
  
 _message_ (**Uint**)
  
Message auquel répondre.
  
 _wParam_ (**WParam**)
  
 _lParam_ (**LParam**)
  
Arguments passés par Windows.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

LRESULT: 0 si le message a été géré, sinon le résultat retourné par la valeur **WndProc**par défaut.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

