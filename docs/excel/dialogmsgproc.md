---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- fonction dialogmsgproc [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782019"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Cette procédure est associée avec la boîte de dialogue Windows native affiche ce [fShowDialog](fshowdialog.md) . Il fournit les routines de service appelées par Windows pour les événements qui se produisent lorsque l’utilisateur fonctionne un des boutons de la boîte de dialogue, les champs d’entrée ou contrôles (messages). 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
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

 **La valeur TRUE** si les messages traités, **FALSE** dans le cas contraire. 
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

