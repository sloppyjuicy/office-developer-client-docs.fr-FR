---
title: xlfUnregister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419904"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="a4329-104">xlfUnregister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="a4329-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="a4329-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a4329-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a4329-106">Peut être appelée à partir d’une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a4329-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="a4329-107">Cela équivaut à appeler **UNREGISTER** à partir d’Excel feuille macro XLM.</span><span class="sxs-lookup"><span data-stu-id="a4329-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="a4329-108">**xlfUnregister** peut être appelé sous deux formes :</span><span class="sxs-lookup"><span data-stu-id="a4329-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="a4329-109">Formulaire 1 : désinsère une commande ou une fonction individuelle.</span><span class="sxs-lookup"><span data-stu-id="a4329-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="a4329-110">Formulaire 2 : décharge et désactive une XLL.</span><span class="sxs-lookup"><span data-stu-id="a4329-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="a4329-111">Appelée dans le formulaire 2, cette fonction force le déchargement complet d’une DLL ou d’une ressource de code.</span><span class="sxs-lookup"><span data-stu-id="a4329-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="a4329-112">Elle désinsère toutes les fonctions dans une DLL, même si elles sont actuellement en cours d’utilisation par une autre macro, quel que soit le nombre d’utilisations.</span><span class="sxs-lookup"><span data-stu-id="a4329-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="a4329-113">Cette fonction appelle **xlAutoClose,** puis désinsère toutes les fonctions dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="a4329-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="a4329-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="a4329-114">Parameters</span></span>

<span data-ttu-id="a4329-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="a4329-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="a4329-116">Nom de la DLL.</span><span class="sxs-lookup"><span data-stu-id="a4329-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a4329-117">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="a4329-117">Property value/Return value</span></span>

<span data-ttu-id="a4329-118">Si elle réussit, renvoie **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="a4329-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="a4329-119">En cas d’échec, renvoie **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a4329-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4329-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4329-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="a4329-121">N’appelez pas cette forme de fonction à partir de votre implémentation de [xlAutoClose](xlautoclose.md) pour tenter d’désinsser toutes les ressources de la DLL à l’aide d’un seul appel de fonction simple.</span><span class="sxs-lookup"><span data-stu-id="a4329-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="a4329-122">Cela entraîne un appel **récursif de xlAutoClose** et un dépassement de la pile.</span><span class="sxs-lookup"><span data-stu-id="a4329-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="a4329-123">N’oubliez pas de supprimer des noms</span><span class="sxs-lookup"><span data-stu-id="a4329-123">Remember to delete names</span></span>

<span data-ttu-id="a4329-124">Si vous avez spécifié l’argument  _pxFunctionText_ à **xlfRegister,** lors de l’inscription des fonctions et commandes de la DLL, vous devez explicitement supprimer les noms en appelant **xlfSetName** pour chacun d’eux, en omettant le deuxième argument afin que la fonction n’apparaisse plus dans l’Assistant Fonction.</span><span class="sxs-lookup"><span data-stu-id="a4329-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="a4329-125">Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="a4329-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a4329-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4329-126">See also</span></span>

- [<span data-ttu-id="a4329-127">xlfRegister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="a4329-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="a4329-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="a4329-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="a4329-129">xlfUnregister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="a4329-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="a4329-130">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="a4329-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

