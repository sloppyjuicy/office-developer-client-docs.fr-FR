---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- fonction xlfsetname [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404259"
---
# <a name="xlfsetname"></a><span data-ttu-id="5a22e-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="5a22e-104">xlfSetName</span></span>

<span data-ttu-id="5a22e-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5a22e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5a22e-106">Utilisé pour créer et supprimer des noms définis associés à la DLL.</span><span class="sxs-lookup"><span data-stu-id="5a22e-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="5a22e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="5a22e-107">Parameters</span></span>

<span data-ttu-id="5a22e-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5a22e-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5a22e-109">Nom de la plage, qui doit être conforme aux limitations habituelles dans Microsoft Excel sur les noms valides.</span><span class="sxs-lookup"><span data-stu-id="5a22e-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="5a22e-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef** ou **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="5a22e-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="5a22e-111">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="5a22e-111">(Optional).</span></span> <span data-ttu-id="5a22e-112">Valeur, ensemble de valeurs, cellule ou plage de cellules définies par _pxNameText._</span><span class="sxs-lookup"><span data-stu-id="5a22e-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="5a22e-113">S’il est omis, le nom est supprimé.</span><span class="sxs-lookup"><span data-stu-id="5a22e-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5a22e-114">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="5a22e-114">Property value/Return value</span></span>

<span data-ttu-id="5a22e-115">_pxRes_ (**xltypeBool** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="5a22e-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="5a22e-116">TRUE si l’opération a réussi ou FALSE si le nom n’a pas pu être créé ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="5a22e-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="5a22e-117">Renvoie #VALUE !</span><span class="sxs-lookup"><span data-stu-id="5a22e-117">Returns #VALUE!</span></span> <span data-ttu-id="5a22e-118">si un ou plusieurs arguments n’étaient pas valides.</span><span class="sxs-lookup"><span data-stu-id="5a22e-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a22e-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a22e-119">Remarks</span></span>

<span data-ttu-id="5a22e-120">Lorsqu’une fonction ou une commande est inscrite à l’aide de **xlfRegister** avec un argument _pxFunctionText_ valide, Excel crée un nom associé à la ressource DLL.</span><span class="sxs-lookup"><span data-stu-id="5a22e-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="5a22e-121">Lorsque votre DLL est déchargée, ces noms doivent être supprimés à l’aide de la [fonction xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="5a22e-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="5a22e-122">Toutefois, en raison d’un problème connu dans Excel, cette opération de suppression échoue.</span><span class="sxs-lookup"><span data-stu-id="5a22e-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="5a22e-123">Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="5a22e-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="5a22e-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="5a22e-124">Example</span></span>

<span data-ttu-id="5a22e-125">Consultez le code de la **fonction xlAutoClose** dans  `\SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="5a22e-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a22e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a22e-126">See also</span></span>

- [<span data-ttu-id="5a22e-127">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="5a22e-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

