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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432491"
---
# <a name="excelcursorproc"></a><span data-ttu-id="a63e8-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="a63e8-104">ExcelCursorProc</span></span>

 <span data-ttu-id="a63e8-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a63e8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a63e8-106">Lorsqu’une boîte de dialogue modale est affichée sur la fenêtre Microsoft Excel, le curseur est un curseur occupé au-dessus de la Excel fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a63e8-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="a63e8-107">Ce **WndProc** capture WM_SETCURSOR type Windows messages et modifie le curseur en flèche normale.</span><span class="sxs-lookup"><span data-stu-id="a63e8-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="a63e8-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="a63e8-108">Parameters</span></span>

 <span data-ttu-id="a63e8-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="a63e8-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="a63e8-110">Contient le handle de Windows HWND de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a63e8-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="a63e8-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="a63e8-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="a63e8-112">Message à répondre.</span><span class="sxs-lookup"><span data-stu-id="a63e8-112">The message to respond to.</span></span>
  
 <span data-ttu-id="a63e8-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="a63e8-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="a63e8-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="a63e8-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="a63e8-115">Arguments transmis par Windows.</span><span class="sxs-lookup"><span data-stu-id="a63e8-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a63e8-116">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="a63e8-116">Property value/Return value</span></span>

<span data-ttu-id="a63e8-117">LRESULT : 0 si le message a été géré, sinon le résultat renvoyé par **le WndProc par défaut**.</span><span class="sxs-lookup"><span data-stu-id="a63e8-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="a63e8-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="a63e8-118">Example</span></span>

<span data-ttu-id="a63e8-119">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a63e8-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a63e8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a63e8-120">See also</span></span>



[<span data-ttu-id="a63e8-121">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="a63e8-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

