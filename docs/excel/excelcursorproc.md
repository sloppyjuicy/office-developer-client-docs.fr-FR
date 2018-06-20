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
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782118"
---
# <a name="excelcursorproc"></a><span data-ttu-id="04bb5-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="04bb5-104">ExcelCursorProc</span></span>

 <span data-ttu-id="04bb5-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="04bb5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="04bb5-106">Lorsqu’une boîte de dialogue modale s’affiche au-dessus de la fenêtre Microsoft Excel, le curseur est un curseur occupé (e) sur la fenêtre Excel.</span><span class="sxs-lookup"><span data-stu-id="04bb5-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="04bb5-107">Cette interruptions **WndProc** WM_SETCURSOR tapez messages Windows et modifications le curseur jusqu'à une flèche normale.</span><span class="sxs-lookup"><span data-stu-id="04bb5-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="04bb5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04bb5-108">Parameters</span></span>

 <span data-ttu-id="04bb5-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="04bb5-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="04bb5-110">Contient un handle HWND Windows de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="04bb5-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="04bb5-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="04bb5-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="04bb5-112">Le message pour répondre à.</span><span class="sxs-lookup"><span data-stu-id="04bb5-112">The message to respond to.</span></span>
  
 <span data-ttu-id="04bb5-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="04bb5-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="04bb5-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="04bb5-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="04bb5-115">Arguments transmis par Windows.</span><span class="sxs-lookup"><span data-stu-id="04bb5-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="04bb5-116">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="04bb5-116">Property value/Return value</span></span>

<span data-ttu-id="04bb5-117">LRESULT : 0 si le message a été géré, sinon le résultat renvoyé par la valeur par défaut **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="04bb5-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="04bb5-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="04bb5-118">Example</span></span>

<span data-ttu-id="04bb5-119">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="04bb5-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04bb5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04bb5-120">See also</span></span>



[<span data-ttu-id="04bb5-121">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="04bb5-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

