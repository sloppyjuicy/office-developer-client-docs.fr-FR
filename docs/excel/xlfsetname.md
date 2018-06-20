---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- fonction xlfSetName [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782218"
---
# <a name="xlfsetname"></a><span data-ttu-id="dc995-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="dc995-104">xlfSetName</span></span>

<span data-ttu-id="dc995-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dc995-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dc995-106">Permet de créer et supprimer des noms définis associés à la DLL.</span><span class="sxs-lookup"><span data-stu-id="dc995-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="dc995-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc995-107">Parameters</span></span>

<span data-ttu-id="dc995-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="dc995-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="dc995-109">Le nom de la plage qui doit être conforme aux limites habituelles dans Microsoft Excel sur les noms valides.</span><span class="sxs-lookup"><span data-stu-id="dc995-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="dc995-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**ou **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="dc995-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="dc995-111">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="dc995-111">(Optional).</span></span> <span data-ttu-id="dc995-112">La valeur, l’ensemble de valeurs, cellule ou plage de cellules que _pxNameText_ est défini en tant que.</span><span class="sxs-lookup"><span data-stu-id="dc995-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="dc995-113">En cas d’omission, le nom est supprimé.</span><span class="sxs-lookup"><span data-stu-id="dc995-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="dc995-114">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dc995-114">Property value/Return value</span></span>

<span data-ttu-id="dc995-115">_pxRes_ (**xltypeBool** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="dc995-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="dc995-116">TRUE si l’opération a réussi, ou FALSE si le nom ne peut pas créer ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="dc995-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="dc995-117">Propriété renvoie #VALUE !</span><span class="sxs-lookup"><span data-stu-id="dc995-117">Returns #VALUE!</span></span> <span data-ttu-id="dc995-118">Si un ou plusieurs des arguments n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="dc995-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc995-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc995-119">Remarks</span></span>

<span data-ttu-id="dc995-120">Lorsqu’une fonction ou une commande est enregistrée à l’aide de **xlfRegister** avec un argument valide _pxFunctionText_ , Excel crée un nom associé à la DLL de ressource.</span><span class="sxs-lookup"><span data-stu-id="dc995-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="dc995-121">Lorsque votre DLL est déchargé, ces noms doivent être supprimés à l’aide de la [fonction xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="dc995-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="dc995-122">Toutefois, en raison d’un problème connu dans Excel, cette opération de suppression échoue.</span><span class="sxs-lookup"><span data-stu-id="dc995-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="dc995-123">Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="dc995-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="dc995-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc995-124">Example</span></span>

<span data-ttu-id="dc995-125">Voir le code de la fonction **xlAutoClose** dans `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="dc995-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc995-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc995-126">See also</span></span>

- [<span data-ttu-id="dc995-127">Fonctions XLM API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="dc995-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

