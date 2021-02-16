---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- fonction xlabort [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436656"
---
# <a name="xlabort"></a><span data-ttu-id="aebcd-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="aebcd-104">xlAbort</span></span>

 <span data-ttu-id="aebcd-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aebcd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aebcd-106">Permet au processeur d’effectuer d’autres tâches dans le système et de vérifier si l’utilisateur a appuyer sur **ÉCHAP** pour annuler une macro.</span><span class="sxs-lookup"><span data-stu-id="aebcd-106">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro.</span></span> <span data-ttu-id="aebcd-107">Si l’utilisateur a appuyer sur **ÉCHAP** pendant le recalcul d’un workbook, il peut également être détecté à partir d’une fonction de feuille de calcul en appelant cette fonction.</span><span class="sxs-lookup"><span data-stu-id="aebcd-107">If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="aebcd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aebcd-108">Parameters</span></span>

 <span data-ttu-id="aebcd-109">_pxRetain_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="aebcd-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="aebcd-110">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="aebcd-110">(Optional).</span></span> <span data-ttu-id="aebcd-111">Si elle a la forme **FALSE,** cette fonction vérifie la condition de rupture et permet d’effacer les coupures en attente.</span><span class="sxs-lookup"><span data-stu-id="aebcd-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="aebcd-112">Cela permet à l’utilisateur de continuer malgré la condition d’coupure.</span><span class="sxs-lookup"><span data-stu-id="aebcd-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="aebcd-113">Si cet argument est omis ou a la valeur **TRUE,** la fonction vérifie si un utilisateur abandonne sans l’effacer.</span><span class="sxs-lookup"><span data-stu-id="aebcd-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="aebcd-114">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="aebcd-114">Property value/Return value</span></span>

<span data-ttu-id="aebcd-115">Renvoie **TRUE** (**xltypeBool**) si l’utilisateur a appuyer sur **ÉCHAP**.</span><span class="sxs-lookup"><span data-stu-id="aebcd-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aebcd-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="aebcd-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="aebcd-117">Des appels fréquents peuvent être nécessaires</span><span class="sxs-lookup"><span data-stu-id="aebcd-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="aebcd-118">Les fonctions et commandes qui peuvent prendre beaucoup de temps doivent appeler cette fonction fréquemment pour donner au processeur d’autres tâches dans le système.</span><span class="sxs-lookup"><span data-stu-id="aebcd-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="aebcd-119">Éviter les langages sensibles</span><span class="sxs-lookup"><span data-stu-id="aebcd-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="aebcd-120">Évitez d’utiliser le terme « Abandonner » dans votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aebcd-120">Avoid using the term "Abort" in your user interface.</span></span> <span data-ttu-id="aebcd-121">Envisagez plutôt d’utiliser « Annuler », « Arrêter », « Arrêter » ou « Arrêter ».</span><span class="sxs-lookup"><span data-stu-id="aebcd-121">Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="aebcd-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="aebcd-122">Example</span></span>

<span data-ttu-id="aebcd-123">Le code suivant déplace à plusieurs reprises la cellule active d’une feuille jusqu’à ce qu’une minute soit écoulée ou jusqu’à ce que l’utilisateur appuie sur **ÉCHAP.**</span><span class="sxs-lookup"><span data-stu-id="aebcd-123">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**.</span></span> <span data-ttu-id="aebcd-124">Il appelle parfois la fonction **xlAbort.**</span><span class="sxs-lookup"><span data-stu-id="aebcd-124">It calls the function **xlAbort** occasionally.</span></span> <span data-ttu-id="aebcd-125">Cela produit le processeur, ce qui facilite la multitâche multinationale.</span><span class="sxs-lookup"><span data-stu-id="aebcd-125">This yields the processor, easing cooperative multitasking.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="aebcd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aebcd-126">See also</span></span>



[<span data-ttu-id="aebcd-127">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="aebcd-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

