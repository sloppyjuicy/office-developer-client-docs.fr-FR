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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782205"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="3183d-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="3183d-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="3183d-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3183d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3183d-106">Supprime **ExcelCursorProc** qui a été précédemment installé par **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="3183d-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="3183d-107">Cette tâche ont effectue afin que **ExcelCursorProc** a été appelé avant **WndProc**Microsoft Excel principale.</span><span class="sxs-lookup"><span data-stu-id="3183d-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="3183d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3183d-108">Parameters</span></span>

 <span data-ttu-id="3183d-109">_hWndExcel_ (**Gérer**)</span><span class="sxs-lookup"><span data-stu-id="3183d-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="3183d-110">La fenêtre principale Excel gère.</span><span class="sxs-lookup"><span data-stu-id="3183d-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3183d-111">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3183d-111">Property value/Return value</span></span>

<span data-ttu-id="3183d-112">La fonction ne retourne pas une valeur.</span><span class="sxs-lookup"><span data-stu-id="3183d-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3183d-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="3183d-113">Remarks</span></span>

<span data-ttu-id="3183d-114">Cette fonction restaure la valeur par défaut Excel **WndProc** pour restaurer l’adresse qui a été enregistré par **HookExcelWindow()** à l’aide de **SetWindowLong()** .</span><span class="sxs-lookup"><span data-stu-id="3183d-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="3183d-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="3183d-115">Example</span></span>

<span data-ttu-id="3183d-116">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3183d-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3183d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3183d-117">See also</span></span>



[<span data-ttu-id="3183d-118">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="3183d-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

