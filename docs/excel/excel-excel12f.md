---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- fonction Excel [excel 2007], fonction Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782055"
---
# <a name="excelexcel12f"></a><span data-ttu-id="166eb-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="166eb-104">Excel/Excel12f</span></span>

 <span data-ttu-id="166eb-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="166eb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="166eb-106">Fonctions de la bibliothèque Framework.</span><span class="sxs-lookup"><span data-stu-id="166eb-106">Framework library functions.</span></span> <span data-ttu-id="166eb-107">**Excel** est un wrapper de la fonction [Excel4](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="166eb-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="166eb-108">**Excel12f** est un wrapper de la fonction [Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="166eb-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="166eb-109">Chaque vérifie qu’aucun des arguments est zéro, ce qui indique que la création d’un temporaire **XLOPER** **XLOPER12** a échoué.</span><span class="sxs-lookup"><span data-stu-id="166eb-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="166eb-110">Si une erreur se produit, chacun affiche un message de débogage.</span><span class="sxs-lookup"><span data-stu-id="166eb-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="166eb-111">Lorsque vous avez terminé, chacun libère toute la mémoire temporaire qui peut ont été créée pour temporaire **XLOPER**et **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="166eb-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="166eb-112">**Excel12f** peut être appelée uniquement à partir d’une DLL à partir de la bibliothèque d’interface API C Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="166eb-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="166eb-113">En outre, il seulement fonctionne lors de l’exécution de démarrage d’Excel 2007 et échoue avec **xlretFailed** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="166eb-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="166eb-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="166eb-114">Parameters</span></span>

 <span data-ttu-id="166eb-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="166eb-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="166eb-116">Un nombre indiquant la commande ou la fonction que vous voulez appeler.</span><span class="sxs-lookup"><span data-stu-id="166eb-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="166eb-117">Pour plus d’informations, voir [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="166eb-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="166eb-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="166eb-118">_pxRes_</span></span>
  
<span data-ttu-id="166eb-119">Un pointeur vers le résultat de la fonction évaluée.</span><span class="sxs-lookup"><span data-stu-id="166eb-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="166eb-120">Mémoire vers lequel pointe dans le résultat sera ont été utilisé par Excel et doit être libéré dans un appel à [xlFree](xlfree.md) une fois qu’il n’est plus nécessaire, ou en définissant **xlbitXLFree** si elle de retour dans Excel.</span><span class="sxs-lookup"><span data-stu-id="166eb-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="166eb-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="166eb-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="166eb-122">Le nombre d’arguments qui sera passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="166eb-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="166eb-123">À compter d’Excel 2007, la limite est de 255 arguments.</span><span class="sxs-lookup"><span data-stu-id="166eb-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="166eb-124">Dans les versions antérieures, la limite est de 30.</span><span class="sxs-lookup"><span data-stu-id="166eb-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="166eb-125">_argument1..._</span><span class="sxs-lookup"><span data-stu-id="166eb-125">_argument1, ..._</span></span>
  
<span data-ttu-id="166eb-126">Les arguments facultatifs à la fonction.</span><span class="sxs-lookup"><span data-stu-id="166eb-126">The optional arguments to the function.</span></span> <span data-ttu-id="166eb-127">Tous les arguments doivent être des pointeurs vers **XLOPER**dans le cas **d’Excel**, ou **XLOPER12**dans le cas **Excel12f**.</span><span class="sxs-lookup"><span data-stu-id="166eb-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="166eb-128">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="166eb-128">Return value</span></span>

<span data-ttu-id="166eb-129">Les deux fonctions renvoient la même erreur et les codes de réussite en tant que **Excel4**, **Excel4v**, **Excel12**et **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="166eb-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="166eb-130">Voir [Excel4/Excel12](excel4-excel12.md) pour une description complète de ces codes.</span><span class="sxs-lookup"><span data-stu-id="166eb-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="166eb-131">En outre, ces fonctions de Framework renvoient **xlretFailed** sans appeler l’API C si un pointeur NULL à un paramètre est détecté.</span><span class="sxs-lookup"><span data-stu-id="166eb-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="166eb-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="166eb-132">Example</span></span>

<span data-ttu-id="166eb-133">Cet exemple transmet un argument non valide pour la fonction **Excel12f** , qui envoie un message pour le débogueur.</span><span class="sxs-lookup"><span data-stu-id="166eb-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="166eb-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="166eb-134">See also</span></span>



[<span data-ttu-id="166eb-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="166eb-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="166eb-136">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="166eb-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

