---
title: xlfUnregister (formulaire 2)
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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782242"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="f5c6c-104">xlfUnregister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="f5c6c-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="f5c6c-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f5c6c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f5c6c-106">Peut être appelée à partir d’une commande DLL ou XLL lui-même a été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="f5c6c-107">Cela équivaut à appeler **Annuler l’inscription** d’une feuille de macro Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="f5c6c-108">**xlfUnregister** peut être appelée sous deux formes :</span><span class="sxs-lookup"><span data-stu-id="f5c6c-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="f5c6c-109">Formulaire 1 : Annule l’enregistrement d’une commande ou une fonction.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="f5c6c-110">Formulaire 2 : Décharge et désactive une solution XLL.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="f5c6c-111">Appelé dans le formulaire 2, cette fonction force une DLL ou ressource de code pour être déchargé entièrement.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="f5c6c-112">Il annule l’inscription de toutes les fonctions dans une DLL, même si elles sont actuellement en cours d’utilisation par une autre macro, quel que soit le compteur d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="f5c6c-113">Cette fonction appelle **xlAutoClose**, puis annule l’enregistrement de toutes les fonctions de la DLL.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="f5c6c-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5c6c-114">Parameters</span></span>

<span data-ttu-id="f5c6c-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="f5c6c-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="f5c6c-116">Le nom de la DLL.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f5c6c-117">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f5c6c-117">Property value/Return value</span></span>

<span data-ttu-id="f5c6c-118">Si l’opération réussit, renvoie **la valeur TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="f5c6c-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="f5c6c-119">En cas d’échec, renvoie **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5c6c-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5c6c-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="f5c6c-121">N’appelez pas cette forme de la fonction à partir de votre implémentation de la [xlAutoClose](xlautoclose.md) lors d’une tentative d’annuler l’inscription de toutes les ressources de la DLL avec l’appel d’une fonction simple.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="f5c6c-122">Cela conduit à l’appel récursif de **xlAutoClose** et un dépassement.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="f5c6c-123">N’oubliez pas de supprimer des noms</span><span class="sxs-lookup"><span data-stu-id="f5c6c-123">Remember to delete names</span></span>

<span data-ttu-id="f5c6c-124">Si vous spécifiez l’argument _pxFunctionText_ de **xlfRegister**, lors de l’inscription des fonctions et les commandes de la DLL, vous devez supprimer explicitement les noms en appelant **xlfSetName** pour chacun d’eux, en omettant le deuxième argument afin que la fonction n’apparaît plus dans l’Assistant fonction.</span><span class="sxs-lookup"><span data-stu-id="f5c6c-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="f5c6c-125">Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="f5c6c-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5c6c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5c6c-126">See also</span></span>

- [<span data-ttu-id="f5c6c-127">xlfRegister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="f5c6c-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="f5c6c-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="f5c6c-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="f5c6c-129">xlfUnregister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="f5c6c-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="f5c6c-130">Fonctions XLM API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="f5c6c-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

