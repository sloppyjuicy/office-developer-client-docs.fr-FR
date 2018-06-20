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
# <a name="dialogmsgproc"></a><span data-ttu-id="82cd0-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="82cd0-104">DIALOGMsgProc</span></span>

<span data-ttu-id="82cd0-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="82cd0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="82cd0-106">Cette procédure est associée avec la boîte de dialogue Windows native affiche ce [fShowDialog](fshowdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="82cd0-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="82cd0-107">Il fournit les routines de service appelées par Windows pour les événements qui se produisent lorsque l’utilisateur fonctionne un des boutons de la boîte de dialogue, les champs d’entrée ou contrôles (messages).</span><span class="sxs-lookup"><span data-stu-id="82cd0-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="82cd0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82cd0-108">Parameters</span></span>

 <span data-ttu-id="82cd0-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="82cd0-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="82cd0-110">Contient un handle HWND Windows de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="82cd0-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="82cd0-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="82cd0-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="82cd0-112">Le message pour répondre à.</span><span class="sxs-lookup"><span data-stu-id="82cd0-112">The message to respond to.</span></span>
  
 <span data-ttu-id="82cd0-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="82cd0-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="82cd0-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="82cd0-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="82cd0-115">Arguments transmis par Windows.</span><span class="sxs-lookup"><span data-stu-id="82cd0-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="82cd0-116">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="82cd0-116">Property value/Return value</span></span>

 <span data-ttu-id="82cd0-117">**La valeur TRUE** si les messages traités, **FALSE** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="82cd0-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="82cd0-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="82cd0-118">Example</span></span>

<span data-ttu-id="82cd0-119">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="82cd0-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82cd0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82cd0-120">See also</span></span>



[<span data-ttu-id="82cd0-121">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="82cd0-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

