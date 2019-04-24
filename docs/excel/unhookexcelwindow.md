---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- fonction UnhookExcelWindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310310"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="cba90-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="cba90-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="cba90-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cba90-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cba90-106">Supprime le **ExcelCursorProc** qui a été précédemment installé par **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="cba90-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="cba90-107">Cette opération aurait été réalisée de sorte que **ExcelCursorProc** ait été appelé avant Microsoft Excel principal **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="cba90-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="cba90-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cba90-108">Parameters</span></span>

 <span data-ttu-id="cba90-109">_hWndExcel_ (**Handle**)</span><span class="sxs-lookup"><span data-stu-id="cba90-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="cba90-110">Le descripteur Windows principal d'Excel.</span><span class="sxs-lookup"><span data-stu-id="cba90-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cba90-111">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="cba90-111">Property value/Return value</span></span>

<span data-ttu-id="cba90-112">La fonction ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cba90-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cba90-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="cba90-113">Remarks</span></span>

<span data-ttu-id="cba90-114">Cette fonction restaure la valeur par défaut \*\*\*\* d'Excel à l'aide de **SetWindowLong ()** pour restaurer l'adresse enregistrée par **HookExcelWindow ()**.</span><span class="sxs-lookup"><span data-stu-id="cba90-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="cba90-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="cba90-115">Example</span></span>

<span data-ttu-id="cba90-116">Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cba90-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cba90-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cba90-117">See also</span></span>



[<span data-ttu-id="cba90-118">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="cba90-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

