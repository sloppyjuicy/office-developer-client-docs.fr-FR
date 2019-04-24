---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- fonction dialogmsgproc [Excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310961"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="c5415-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="c5415-104">DIALOGMsgProc</span></span>

<span data-ttu-id="c5415-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c5415-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c5415-106">Cette procédure est associée à la boîte de dialogue Windows Native affichée par [fShowDialog](fshowdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c5415-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="c5415-107">Il fournit les routines de service appelées par Windows pour les événements (messages) qui se produisent lorsque l'utilisateur utilise l'un des boutons, champs d'entrée ou contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c5415-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="c5415-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5415-108">Parameters</span></span>

 <span data-ttu-id="c5415-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="c5415-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="c5415-110">Contient le handle Windows HWND de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c5415-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="c5415-111">_message_ (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="c5415-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="c5415-112">Message auquel répondre.</span><span class="sxs-lookup"><span data-stu-id="c5415-112">The message to respond to.</span></span>
  
 <span data-ttu-id="c5415-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="c5415-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="c5415-114">_lParam_ (**LParam**)</span><span class="sxs-lookup"><span data-stu-id="c5415-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="c5415-115">Arguments passés par Windows.</span><span class="sxs-lookup"><span data-stu-id="c5415-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c5415-116">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="c5415-116">Property value/Return value</span></span>

 <span data-ttu-id="c5415-117">**True** si le message a \*\*\*\* été traité, false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c5415-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="c5415-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="c5415-118">Example</span></span>

<span data-ttu-id="c5415-119">Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c5415-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5415-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5415-120">See also</span></span>



[<span data-ttu-id="c5415-121">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="c5415-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

