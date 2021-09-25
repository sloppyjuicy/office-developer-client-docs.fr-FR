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
ms.localizationpriority: medium
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f93be01679460833d9555cc747ff72d9b1d5b6fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625965"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Cette procédure est associée à la boîte de dialogue Windows native que [fShowDialog](fshowdialog.md) affiche. Il fournit les routines de service appelées par Windows pour les événements (messages) qui se produisent lorsque l’utilisateur exploite l’un des boutons, champs d’entrée ou contrôles de la boîte de dialogue. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
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

 **TRUE** si le message est traitée, **FALSE** si ce n’est pas le cas. 
  
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

