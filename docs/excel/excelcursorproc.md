---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- fonction excelcursorproc [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782118"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Lorsqu’une boîte de dialogue modale s’affiche au-dessus de la fenêtre Microsoft Excel, le curseur est un curseur occupé (e) sur la fenêtre Excel. Cette interruptions **WndProc** WM_SETCURSOR tapez messages Windows et modifications le curseur jusqu'à une flèche normale. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Paramètres

 _hWndDlg_ (**HWND**)
  
Contient un handle HWND Windows de la boîte de dialogue.
  
 _message_ (**UINT**)
  
Le message pour répondre à.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Arguments transmis par Windows.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

LRESULT : 0 si le message a été géré, sinon le résultat renvoyé par la valeur par défaut **WndProc**.
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

