---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- fonction xlAbort [Excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310254"
---
# <a name="xlabort"></a>xlAbort

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Permet au processeur d'effectuer d'autres tâches dans le système et vérifie si l'utilisateur a appuyé sur **Échap** pour annuler une macro. Si l'utilisateur a appuyé sur **Échap** pendant le recalcul d'un classeur, il est également possible de le détecter à partir d'une fonction de feuille de calcul en appelant cette fonction. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Paramètres

 _pxRetain_ (**xltypeBool**)
  
(Facultatif). Si la **valeur**est false, cette fonction vérifie la condition d'arrêt et efface tout arrêt en attente. Cela permet à l'utilisateur de continuer malgré la condition d'arrêt. Si cet argument est omis ou s'il a la **valeur true**, la fonction vérifie l'abandon de l'utilisateur sans l'effacer.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Renvoie la **valeur true** (**xltypeBool**) si l'utilisateur a appuyé sur **Échap**.
  
## <a name="remarks"></a>Remarques

### 

#### <a name="frequent-calls-may-be-needed"></a>Des appels fréquents peuvent être nécessaires

Les fonctions et les commandes pouvant prendre beaucoup de temps doivent appeler cette fonction fréquemment pour transmettre le processeur à d'autres tâches du système.
  
#### <a name="avoid-sensitive-language"></a>Éviter les langues sensibles

Évitez d'utiliser le terme «Abort» dans votre interface utilisateur. EnVisagez d'utiliser à la place «annuler», «arrêter», «arrêter» ou «arrêter».
  
## <a name="example"></a>Exemple

Le code suivant déplace de manière répétée la cellule active dans une feuille jusqu'à ce que l'utilisateur appuie sur **Échap**. Il appelle de manière occasionnelle la fonction **xlAbort** . Cela permet au processeur de simplifier le multitâche coopératif. 
  
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



[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

