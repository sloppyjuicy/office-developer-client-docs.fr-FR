---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- fonction unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409446"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="6fd7a-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="6fd7a-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="6fd7a-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6fd7a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6fd7a-106">Supprime **l’ExcelCursorProc** qui a été précédemment installé par **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="6fd7a-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="6fd7a-107">Cela aurait été fait pour **qu’ExcelCursorProc** soit appelé avant le **WndProc** principal de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6fd7a-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="6fd7a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fd7a-108">Parameters</span></span>

 <span data-ttu-id="6fd7a-109">_hWndExcel_ (**HANDLE**)</span><span class="sxs-lookup"><span data-stu-id="6fd7a-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="6fd7a-110">Handle Windows principal Excel.</span><span class="sxs-lookup"><span data-stu-id="6fd7a-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6fd7a-111">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="6fd7a-111">Property value/Return value</span></span>

<span data-ttu-id="6fd7a-112">La fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6fd7a-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6fd7a-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="6fd7a-113">Remarks</span></span>

<span data-ttu-id="6fd7a-114">Cette fonction restaure le **WndProc** Par défaut d’Excel à l’aide de **SetWindowLong()** pour restaurer l’adresse qui a été enregistrée par **HookExcelWindow()**.</span><span class="sxs-lookup"><span data-stu-id="6fd7a-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="6fd7a-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="6fd7a-115">Example</span></span>

<span data-ttu-id="6fd7a-116">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6fd7a-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fd7a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fd7a-117">See also</span></span>



[<span data-ttu-id="6fd7a-118">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="6fd7a-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

