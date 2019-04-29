---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- fonction xlfRegisterId [Excel 2007]
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
# <a name="xlfregisterid"></a><span data-ttu-id="bed3e-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="bed3e-104">xlfRegisterId</span></span>

<span data-ttu-id="bed3e-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bed3e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bed3e-106">Peut être appelé à partir d'une DLL qui a elle-même été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bed3e-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="bed3e-107">Si une fonction est déjà inscrite, elle renvoie l'ID de Registre existant pour cette fonction sans la réenregistrer.</span><span class="sxs-lookup"><span data-stu-id="bed3e-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="bed3e-108">Si une fonction n'est pas encore enregistrée, elle l'enregistre et renvoie l'ID de Registre résultant.</span><span class="sxs-lookup"><span data-stu-id="bed3e-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="bed3e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bed3e-109">Parameters</span></span>

<span data-ttu-id="bed3e-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="bed3e-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="bed3e-111">Nom de la DLL contenant la fonction.</span><span class="sxs-lookup"><span data-stu-id="bed3e-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="bed3e-112">_pxProcedure_ (**xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="bed3e-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="bed3e-113">Si une chaîne, nom de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="bed3e-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="bed3e-114">S'il s'agit d'un nombre, le numéro d'export ordinal de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="bed3e-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="bed3e-115">Pour des fins de clarté et de robustesse, utilisez toujours le formulaire de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bed3e-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="bed3e-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="bed3e-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="bed3e-117">Chaîne facultative spécifiant les types de tous les arguments de la fonction et le type de la valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="bed3e-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="bed3e-118">Pour plus d'informations, reportez-vous à la section «Remarques».</span><span class="sxs-lookup"><span data-stu-id="bed3e-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="bed3e-119">Cet argument peut être omis pour une DLL autonome qui définit **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="bed3e-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bed3e-120">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="bed3e-120">Property value/Return value</span></span>

<span data-ttu-id="bed3e-121">Renvoie l'ID de la fonction (**xltypeNum**), qui peut être utilisée dans les appels ultérieurs à **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="bed3e-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bed3e-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="bed3e-122">Remarks</span></span>

<span data-ttu-id="bed3e-123">Cette fonction est utile lorsque vous ne souhaitez pas vous soucier de la conservation d'un ID de Registre, mais vous en aurez besoin plus tard pour annuler l'inscription.</span><span class="sxs-lookup"><span data-stu-id="bed3e-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="bed3e-124">Il est également utile pour affecter des menus, des outils et des boutons lorsque la fonction que vous souhaitez affecter se trouve dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="bed3e-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="bed3e-125">Lorsqu'une fonction DLL ou XLL a été enregistrée avec un argument _pxFunctionText_ valide ayant été fourni à **XLFREGISTER**, son ID de Registre peut également être obtenu en transmettant la _pxFunctionText_ à la fonction **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="bed3e-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bed3e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bed3e-126">See also</span></span>

- [<span data-ttu-id="bed3e-127">CASIER</span><span class="sxs-lookup"><span data-stu-id="bed3e-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="bed3e-128">ANNULER l'inscription</span><span class="sxs-lookup"><span data-stu-id="bed3e-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="bed3e-129">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="bed3e-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

