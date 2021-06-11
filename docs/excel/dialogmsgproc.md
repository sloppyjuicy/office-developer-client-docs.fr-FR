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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406513"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="fe11f-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="fe11f-104">DIALOGMsgProc</span></span>

<span data-ttu-id="fe11f-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fe11f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fe11f-106">Cette procédure est associée à la boîte de dialogue Windows native que [fShowDialog](fshowdialog.md) affiche.</span><span class="sxs-lookup"><span data-stu-id="fe11f-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="fe11f-107">Il fournit les routines de service appelées par Windows pour les événements (messages) qui se produisent lorsque l’utilisateur exploite l’un des boutons, champs d’entrée ou contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fe11f-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="fe11f-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="fe11f-108">Parameters</span></span>

 <span data-ttu-id="fe11f-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="fe11f-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="fe11f-110">Contient le handle de Windows HWND de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fe11f-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="fe11f-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="fe11f-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="fe11f-112">Message à répondre.</span><span class="sxs-lookup"><span data-stu-id="fe11f-112">The message to respond to.</span></span>
  
 <span data-ttu-id="fe11f-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="fe11f-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="fe11f-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="fe11f-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="fe11f-115">Arguments transmis par Windows.</span><span class="sxs-lookup"><span data-stu-id="fe11f-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fe11f-116">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="fe11f-116">Property value/Return value</span></span>

 <span data-ttu-id="fe11f-117">**TRUE** si le message est traitée, **FALSE** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="fe11f-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="fe11f-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe11f-118">Example</span></span>

<span data-ttu-id="fe11f-119">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="fe11f-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe11f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe11f-120">See also</span></span>



[<span data-ttu-id="fe11f-121">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="fe11f-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

