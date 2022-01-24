---
title: DIALOGMsgProc
manager: lindalu
ms.date: 1/22/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- fonction dialogmsgproc [excel 2007]
ms.localizationpriority: medium
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2313ea2fe9fbee434260f998127ab269a0125565
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180690"
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

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.
  
## <a name="see-also"></a>Voir aussi

[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)
