---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- fonction Excel [Excel 2007], fonction Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310912"
---
# <a name="excelexcel12f"></a><span data-ttu-id="baf5a-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="baf5a-104">Excel/Excel12f</span></span>

 <span data-ttu-id="baf5a-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="baf5a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="baf5a-106">Fonctions de la bibliothèque Framework.</span><span class="sxs-lookup"><span data-stu-id="baf5a-106">Framework library functions.</span></span> <span data-ttu-id="baf5a-107">**Excel** est un wrapper de la fonction [Excel4](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="baf5a-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="baf5a-108">**Excel12f** est un wrapper de la fonction [Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="baf5a-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="baf5a-109">Chaque contrôle vérifie qu'aucun des arguments n'a la valeur zéro, ce qui signifie que la création d'un élément **XLOPER** ou **XLOPER12** temporaire a échoué.</span><span class="sxs-lookup"><span data-stu-id="baf5a-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="baf5a-110">Si une erreur se produit, chacune imprime un message de débogage.</span><span class="sxs-lookup"><span data-stu-id="baf5a-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="baf5a-111">Lorsque vous avez terminé, chaque opération libère la totalité de la mémoire temporaire qui a pu être créée pour les objets **XLOPER**et **XLOPER12**temporaires.</span><span class="sxs-lookup"><span data-stu-id="baf5a-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="baf5a-112">**Excel12f** peut uniquement être appelé à partir d'une dll à partir de la bibliothèque d'API C d'Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="baf5a-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="baf5a-113">En outre, elle ne fonctionne qu'avec Excel 2007, et échoue avec **xlretFailed** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="baf5a-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="baf5a-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="baf5a-114">Parameters</span></span>

 <span data-ttu-id="baf5a-115">_IFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="baf5a-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="baf5a-116">Nombre indiquant la commande ou la fonction que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="baf5a-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="baf5a-117">Pour plus d'informations, consultez la rubrique [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="baf5a-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="baf5a-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="baf5a-118">_pxRes_</span></span>
  
<span data-ttu-id="baf5a-119">Pointeur vers le résultat de la fonction évaluée.</span><span class="sxs-lookup"><span data-stu-id="baf5a-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="baf5a-120">Toute mémoire pointée dans le résultat est allouée par Excel et doit être libérée dans un appel à [xlFree](xlfree.md) une fois qu'elle n'est plus nécessaire, ou en définissant **xlbitXLFree** si elle est renvoyée à Excel.</span><span class="sxs-lookup"><span data-stu-id="baf5a-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="baf5a-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="baf5a-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="baf5a-122">Nombre d'arguments qui seront transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="baf5a-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="baf5a-123">À partir d'Excel 2007, la limite est de 255 arguments.</span><span class="sxs-lookup"><span data-stu-id="baf5a-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="baf5a-124">Dans les versions antérieures, la limite est de 30.</span><span class="sxs-lookup"><span data-stu-id="baf5a-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="baf5a-125">_argument1,..._</span><span class="sxs-lookup"><span data-stu-id="baf5a-125">_argument1, ..._</span></span>
  
<span data-ttu-id="baf5a-126">Arguments facultatifs de la fonction.</span><span class="sxs-lookup"><span data-stu-id="baf5a-126">The optional arguments to the function.</span></span> <span data-ttu-id="baf5a-127">Tous les arguments doivent être des pointeurs vers des objets **XLOPER**dans le cas d' **Excel**ou de **XLOPER12**s dans le cas de **Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="baf5a-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="baf5a-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="baf5a-128">Return value</span></span>

<span data-ttu-id="baf5a-129">Ces deux fonctions renvoient les mêmes codes d'erreur et de succès que **Excel4**, **Excel4v**, **Excel12**et **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="baf5a-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="baf5a-130">Pour une description complète de ces codes, voir [Excel4/Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="baf5a-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="baf5a-131">En outre, ces fonctions d'infrastructure renvoient **xlretFailed** sans appeler l'API C si un pointeur null vers un paramètre est détecté.</span><span class="sxs-lookup"><span data-stu-id="baf5a-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="baf5a-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="baf5a-132">Example</span></span>

<span data-ttu-id="baf5a-133">Cet exemple transmet un argument incorrect à la fonction **Excel12f** , qui envoie un message au débogueur.</span><span class="sxs-lookup"><span data-stu-id="baf5a-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="baf5a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baf5a-134">See also</span></span>



[<span data-ttu-id="baf5a-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="baf5a-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="baf5a-136">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="baf5a-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

