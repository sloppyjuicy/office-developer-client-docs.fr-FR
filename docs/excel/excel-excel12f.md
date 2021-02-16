---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- fonction Excel [excel 2007],fonction Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431672"
---
# <a name="excelexcel12f"></a><span data-ttu-id="53409-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="53409-104">Excel/Excel12f</span></span>

 <span data-ttu-id="53409-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="53409-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="53409-106">Fonctions de bibliothèque d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="53409-106">Framework library functions.</span></span> <span data-ttu-id="53409-107">**Excel** est un wrapper pour la [fonction Excel4.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="53409-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="53409-108">**Excel12f est** un wrapper pour la [fonction Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="53409-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="53409-109">Chaque vérification vérifie qu’aucun des arguments n’est nul, ce qui indique que la création d’une **XLOPER** ou **d’une XLOPER12** temporaire a échoué.</span><span class="sxs-lookup"><span data-stu-id="53409-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="53409-110">Si une erreur se produit, chacun imprime un message de débogage.</span><span class="sxs-lookup"><span data-stu-id="53409-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="53409-111">Lorsque vous avez terminé, chacune libère toute la mémoire temporaire qui a peut-être été créée pour les **xlOPER** et **XLOPER12** temporaires.</span><span class="sxs-lookup"><span data-stu-id="53409-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER** s and **XLOPER12** s.</span></span>
  
 <span data-ttu-id="53409-112">**Excel12f ne** peut être appelé qu’à partir d’une DLL commençant par la bibliothèque d’API C d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="53409-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="53409-113">En outre, il fonctionne uniquement lors de l’exécution à partir d’Excel 2007 et échoue avec **xlretFailed dans le** cas contraire.</span><span class="sxs-lookup"><span data-stu-id="53409-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="53409-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53409-114">Parameters</span></span>

 <span data-ttu-id="53409-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="53409-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="53409-116">Numéro indiquant la commande ou la fonction que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="53409-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="53409-117">Pour plus d’informations, [voir Excel4/Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="53409-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="53409-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="53409-118">_pxRes_</span></span>
  
<span data-ttu-id="53409-119">Pointeur vers le résultat de la fonction évaluée.</span><span class="sxs-lookup"><span data-stu-id="53409-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="53409-120">Toute mémoire pointée vers le résultat a été allouée par Excel et doit être libérée dans un appel à [xlFree](xlfree.md) une fois qu’elle n’est plus nécessaire, ou en paramètre **xlbitXLFree** en cas de renvoi vers Excel.</span><span class="sxs-lookup"><span data-stu-id="53409-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="53409-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="53409-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="53409-122">Nombre d’arguments qui seront transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="53409-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="53409-123">À compter d’Excel 2007, la limite est de 255 arguments.</span><span class="sxs-lookup"><span data-stu-id="53409-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="53409-124">Dans les versions antérieures, la limite est de 30.</span><span class="sxs-lookup"><span data-stu-id="53409-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="53409-125">_argument1, ..._</span><span class="sxs-lookup"><span data-stu-id="53409-125">_argument1, ..._</span></span>
  
<span data-ttu-id="53409-126">Arguments facultatifs de la fonction.</span><span class="sxs-lookup"><span data-stu-id="53409-126">The optional arguments to the function.</span></span> <span data-ttu-id="53409-127">Tous les arguments doivent être des pointeurs vers **xlOPER** s dans le cas **d’Excel**, ou **XLOPER12** s dans le cas **d’Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="53409-127">All arguments must be pointers to **XLOPER** s in the case of **Excel**, or **XLOPER12** s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="53409-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53409-128">Return value</span></span>

<span data-ttu-id="53409-129">Les deux fonctions retournent les mêmes codes d’erreur et de réussite **qu’Excel4,** **Excel4v,** **Excel12** et **Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="53409-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="53409-130">Pour obtenir une description complète de ces codes, voir [Excel4/Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="53409-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="53409-131">En outre, ces fonctions Framework retournent **xlretFailed** sans appeler l’API C si un pointeur NULL vers un paramètre est détecté.</span><span class="sxs-lookup"><span data-stu-id="53409-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="53409-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="53409-132">Example</span></span>

<span data-ttu-id="53409-133">Cet exemple transmet un argument non positif à la fonction **Excel12f,** qui envoie un message au débogger.</span><span class="sxs-lookup"><span data-stu-id="53409-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="53409-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53409-134">See also</span></span>



[<span data-ttu-id="53409-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="53409-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="53409-136">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="53409-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

