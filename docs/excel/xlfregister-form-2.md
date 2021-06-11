---
title: xlfRegister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfregister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416040"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="f10d9-104">xlfRegister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="f10d9-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="f10d9-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f10d9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f10d9-106">Peut être appelée à partir d’une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f10d9-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="f10d9-107">Cela équivaut à appeler **REGISTER** à partir d’Excel feuille macro XLM.</span><span class="sxs-lookup"><span data-stu-id="f10d9-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="f10d9-108">La **fonction xlfRegister** peut être appelée sous deux formes :</span><span class="sxs-lookup"><span data-stu-id="f10d9-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="f10d9-109">[xlfRegister (formulaire 1)](xlfregister-form-1.md): inscrit une commande ou une fonction individuelle.</span><span class="sxs-lookup"><span data-stu-id="f10d9-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="f10d9-110">xlfRegister (formulaire 2) : charge et active une XLL.</span><span class="sxs-lookup"><span data-stu-id="f10d9-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="f10d9-111">Appelée dans le formulaire 2, cette fonction ne peut être utilisée que pour charger et activer une XLL contenant une procédure [xlAutoOpen.](xlautoopen.md)</span><span class="sxs-lookup"><span data-stu-id="f10d9-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="f10d9-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f10d9-112">Parameters</span></span>

 <span data-ttu-id="f10d9-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="f10d9-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="f10d9-114">Nom de la DLL à charger et à activer.</span><span class="sxs-lookup"><span data-stu-id="f10d9-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f10d9-115">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="f10d9-115">Property value/Return value</span></span>

<span data-ttu-id="f10d9-116">Si elle réussit, cela renvoie le nom de la DLL (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="f10d9-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="f10d9-117">Sinon, elle renvoie une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="f10d9-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="f10d9-118">erreur.</span><span class="sxs-lookup"><span data-stu-id="f10d9-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f10d9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f10d9-119">See also</span></span>



[<span data-ttu-id="f10d9-120">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="f10d9-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

