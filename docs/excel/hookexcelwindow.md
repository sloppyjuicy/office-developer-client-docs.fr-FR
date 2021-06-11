---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- fonction hookexcelwindow [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413506"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="69667-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="69667-104">HookExcelWindow</span></span>

 <span data-ttu-id="69667-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="69667-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="69667-106">Installe **ExcelCursorProc** afin qu’il soit appelé avant le Microsoft Excel **principal WndProc**.</span><span class="sxs-lookup"><span data-stu-id="69667-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="69667-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="69667-107">Parameters</span></span>

 <span data-ttu-id="69667-108">_hWndExcel_ (**HANDLE**)</span><span class="sxs-lookup"><span data-stu-id="69667-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="69667-109">Le Excel de Windows principal.</span><span class="sxs-lookup"><span data-stu-id="69667-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="69667-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="69667-110">Property value/Return value</span></span>

<span data-ttu-id="69667-111">La fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="69667-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69667-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="69667-112">Remarks</span></span>

<span data-ttu-id="69667-113">La fonction obtient l’adresse du Excel **WndProc** via l’utilisation de **GetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="69667-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="69667-114">Elle stocke cette valeur dans un global qui peut être utilisé pour appeler le **WndProc** par défaut et également pour la restaurer.</span><span class="sxs-lookup"><span data-stu-id="69667-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="69667-115">Enfin, elle remplace cette adresse par l’adresse **d’ExcelCursorProc** à l’aide **de SetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="69667-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="69667-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="69667-116">Example</span></span>

<span data-ttu-id="69667-117">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="69667-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69667-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69667-118">See also</span></span>



[<span data-ttu-id="69667-119">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="69667-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

