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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782232"
---
# <a name="xlfregisterid"></a><span data-ttu-id="52694-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="52694-104">xlfRegisterId</span></span>

<span data-ttu-id="52694-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52694-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52694-106">Peut être appelée à partir d’une DLL lui-même a été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="52694-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="52694-107">Si une fonction est déjà enregistrée, elle renvoie l’identificateur de Registre existant de la fonction sans réinscription il.</span><span class="sxs-lookup"><span data-stu-id="52694-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="52694-108">Si une fonction n’est pas encore inscrit, il enregistre et renvoie l’identificateur de Registre qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="52694-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="52694-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52694-109">Parameters</span></span>

<span data-ttu-id="52694-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="52694-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="52694-111">Le nom de la DLL contenant la fonction.</span><span class="sxs-lookup"><span data-stu-id="52694-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="52694-112">_pxProcedure_ (**xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="52694-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="52694-113">Si aucune chaîne, le nom de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="52694-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="52694-114">Si un nombre, la propriété ordinal exporter nombre de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="52694-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="52694-115">Pour plus de clarté et robustesse, utilisez toujours la forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="52694-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="52694-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="52694-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="52694-117">Chaîne facultative spécifiant les types de tous les arguments de la fonction et le type de la valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="52694-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="52694-118">Pour plus d’informations, voir la section « Remarques ».</span><span class="sxs-lookup"><span data-stu-id="52694-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="52694-119">Cet argument peut être omis pour une autonome DLL (XLL) définition **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="52694-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="52694-120">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="52694-120">Property value/Return value</span></span>

<span data-ttu-id="52694-121">Renvoie l’identificateur de Registre de la fonction (**xltypeNum**), qui peut être utilisée dans les appels suivants à **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="52694-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52694-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="52694-122">Remarks</span></span>

<span data-ttu-id="52694-123">Cette fonction est utile lorsque vous ne souhaitez pas à se soucier de maintenir un ID de Registre, mais vous devez une version ultérieure pour annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="52694-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="52694-124">Il est également utile pour l’affectation à des outils, des menus et des boutons lorsque la fonction que vous voulez attribuer est dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="52694-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="52694-125">Lorsqu’une fonction DLL ou XLL a été enregistrée avec un argument valide _pxFunctionText_ ayant été fourni à **xlfRegister**, son ID registre peut également être obtenu en transmettant le _pxFunctionText_ à la fonction **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="52694-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="52694-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52694-126">See also</span></span>

- [<span data-ttu-id="52694-127">INSCRIRE</span><span class="sxs-lookup"><span data-stu-id="52694-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="52694-128">ANNULER L’INSCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52694-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="52694-129">Fonctions XLM API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="52694-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

