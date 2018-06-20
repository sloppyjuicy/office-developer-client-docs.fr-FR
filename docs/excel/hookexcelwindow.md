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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782137"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="0f1b2-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="0f1b2-104">HookExcelWindow</span></span>

 <span data-ttu-id="0f1b2-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0f1b2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0f1b2-106">Installe **ExcelCursorProc** afin qu’elle est appelée avant **WndProc**Microsoft Excel principale.</span><span class="sxs-lookup"><span data-stu-id="0f1b2-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="0f1b2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f1b2-107">Parameters</span></span>

 <span data-ttu-id="0f1b2-108">_hWndExcel_ (**Gérer**)</span><span class="sxs-lookup"><span data-stu-id="0f1b2-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="0f1b2-109">La fenêtre principale Excel gère.</span><span class="sxs-lookup"><span data-stu-id="0f1b2-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0f1b2-110">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0f1b2-110">Property value/Return value</span></span>

<span data-ttu-id="0f1b2-111">La fonction ne retourne pas une valeur.</span><span class="sxs-lookup"><span data-stu-id="0f1b2-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0f1b2-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f1b2-112">Remarks</span></span>

<span data-ttu-id="0f1b2-113">La fonction obtient l’adresse d' Excel **WndProc** **GetWindowLong()** grâce à l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0f1b2-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="0f1b2-114">Il stocke cette valeur dans global qui peut être utilisée pour appeler la valeur par défaut **WndProc** et également pour la restaurer.</span><span class="sxs-lookup"><span data-stu-id="0f1b2-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="0f1b2-115">Enfin, il remplace cette adresse avec l’adresse **ExcelCursorProc** à l’aide de **SetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="0f1b2-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="0f1b2-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="0f1b2-116">Example</span></span>

<span data-ttu-id="0f1b2-117">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="0f1b2-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f1b2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f1b2-118">See also</span></span>



[<span data-ttu-id="0f1b2-119">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="0f1b2-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

