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
ms.localizationpriority: medium
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 621a03c00ee4d1509edd3dd8b14a11dba9ba719a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584926"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Lorsqu’une boîte de dialogue modale est affichée sur la fenêtre Microsoft Excel, le curseur est un curseur occupé au-dessus de la Excel fenêtre. Ce **WndProc** capture WM_SETCURSOR type Windows messages et modifie le curseur en flèche normale. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Paramètres

 _hWndDlg_ (**HWND**)
  
Contient le handle de Windows HWND de la boîte de dialogue.
  
 _message_ (**UINT**)
  
Message à répondre.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Arguments transmis par Windows.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

LRESULT : 0 si le message a été géré, sinon le résultat renvoyé par **le WndProc par défaut**.
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

