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
ms.openlocfilehash: e092b1b4823c334b1fae31440a9b7f8ceb928a7b
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199443"
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

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

