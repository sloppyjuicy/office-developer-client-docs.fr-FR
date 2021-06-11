---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- fonction xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420058"
---
# <a name="xlfregisterid"></a><span data-ttu-id="4a043-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="4a043-104">xlfRegisterId</span></span>

<span data-ttu-id="4a043-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4a043-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4a043-106">Peut être appelée à partir d’une DLL qui a elle-même été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4a043-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="4a043-107">Si une fonction est déjà inscrite, elle renvoie l’ID de registre existant pour cette fonction sans l’réinsister.</span><span class="sxs-lookup"><span data-stu-id="4a043-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="4a043-108">Si une fonction n’est pas encore inscrite, elle l’inscrit et renvoie l’ID de registre résultant.</span><span class="sxs-lookup"><span data-stu-id="4a043-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="4a043-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a043-109">Parameters</span></span>

<span data-ttu-id="4a043-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="4a043-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="4a043-111">Nom de la DLL contenant la fonction.</span><span class="sxs-lookup"><span data-stu-id="4a043-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="4a043-112">_pxProcedure_ (**xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="4a043-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="4a043-113">S’il s’agit d’une chaîne, le nom de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="4a043-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="4a043-114">S’il s’agit d’un nombre, le numéro d’exportation ordinal de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="4a043-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="4a043-115">Pour plus de clarté et de robustesse, utilisez toujours la forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="4a043-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="4a043-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="4a043-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="4a043-117">Chaîne facultative spécifiant les types de tous les arguments de la fonction et le type de la valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4a043-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="4a043-118">Pour plus d’informations, voir la section « Remarques ».</span><span class="sxs-lookup"><span data-stu-id="4a043-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="4a043-119">Cet argument peut être omis pour une DLL (XLL) autonome définissant **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="4a043-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4a043-120">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="4a043-120">Property value/Return value</span></span>

<span data-ttu-id="4a043-121">Renvoie l’ID de registre de la fonction (**xltypeNum**), qui peut être utilisé dans les appels ultérieurs **à xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="4a043-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a043-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a043-122">Remarks</span></span>

<span data-ttu-id="4a043-123">Cette fonction est utile lorsque vous ne souhaitez pas vous soucier de la maintenance d’un ID de registre, mais vous en avez besoin ultérieurement pour l’inscription.</span><span class="sxs-lookup"><span data-stu-id="4a043-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="4a043-124">Il est également utile pour affecter des menus, des outils et des boutons lorsque la fonction que vous souhaitez affecter se trouve dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="4a043-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="4a043-125">Lorsqu’une fonction DLL ou XLL a été inscrite avec un argument  _pxFunctionText_ valide ayant été fourni à **xlfRegister**, son ID de registre peut également être obtenu en passant  _le pxFunctionText_ à la fonction **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="4a043-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a043-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a043-126">See also</span></span>

- [<span data-ttu-id="4a043-127">REGISTER</span><span class="sxs-lookup"><span data-stu-id="4a043-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="4a043-128">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="4a043-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="4a043-129">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="4a043-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

