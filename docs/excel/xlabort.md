---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- fonction xlAbort [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e90cbe496404b4cc602dee1ad21c91c8f5f91bfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782211"
---
# <a name="xlabort"></a>xlAbort

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Génère le processeur à d’autres tâches dans le système et vérifie si l’utilisateur a appuyé sur **ÉCHAP** pour annuler une macro. Si l’utilisateur a appuyé sur **ÉCHAP** pendant un recalcul du classeur, il peut également être détectée à partir d’une fonction de feuille de calcul en appelant cette fonction. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Paramètres

 _pxRetain_ (**xltypeBool**)
  
(Facultatif). Si **FALSE**, cette fonction vérifie la condition d’arrêt et efface un arrêt en attente. Cela permet à l’utilisateur de continuer malgré la condition d’arrêt. Si cet argument est omis ou a la **valeur TRUE**, la fonction vérifie un abandon de l’utilisateur sans effacer le contenu.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Retourne **la valeur TRUE** (**xltypeBool**) si l’utilisateur a appuyé sur **ÉCHAP**.
  
## <a name="remarks"></a>Remarques

### 

#### <a name="frequent-calls-may-be-needed"></a>Appels fréquents peuvent être nécessaire.

Fonctions et les commandes qui peuvent prendre beaucoup de temps doivent appeler cette fonction fréquemment pour produire le processeur à d’autres tâches dans le système.
  
#### <a name="avoid-sensitive-language"></a>Éviter de langue sensible

Évitez d’utiliser le terme « Abandonner » dans l’interface utilisateur. Envisagez d’utiliser des « Annuler », « Arrêt », « Saut » ou « Stop » à la place.
  
## <a name="example"></a>Exemple

Le code suivant déplace à plusieurs reprises la cellule active dans une feuille jusqu'à ce qu’une minute écoulée ou jusqu'à ce que l’utilisateur appuie sur **ÉCHAP**. Il appelle la fonction **xlAbort** occasionnellement. Cela donne le processeur et accélération multitâche coopératif. 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

