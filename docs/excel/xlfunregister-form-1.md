---
title: xlfUnregister (formulaire 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- fonction xlfUnregister [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303891"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="a8b21-104">xlfUnregister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="a8b21-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="a8b21-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8b21-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a8b21-106">Peut être appelée à partir d'une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a8b21-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="a8b21-107">Cela équivaut à appeler **Unregister** à partir d'une feuille macro XLM Excel.</span><span class="sxs-lookup"><span data-stu-id="a8b21-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="a8b21-108">**xlfUnregister** peut être appelé sous deux formes:</span><span class="sxs-lookup"><span data-stu-id="a8b21-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="a8b21-109">Formulaire 1: annule l'inscription d'une commande ou d'une fonction individuelle.</span><span class="sxs-lookup"><span data-stu-id="a8b21-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="a8b21-110">Formulaire 2: décharge et désactive un XLL.</span><span class="sxs-lookup"><span data-stu-id="a8b21-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="a8b21-111">Appelée dans le formulaire 1, cette fonction réduit le nombre d'utilisations d'une fonction ou commande DLL précédemment inscrite à l'aide de **xlfRegister** ou **Register**.</span><span class="sxs-lookup"><span data-stu-id="a8b21-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="a8b21-112">Si le nombre d'utilisations est déjà égal à zéro, cette fonction n'a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="a8b21-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="a8b21-113">Lorsque le nombre d'utilisations de toutes les fonctions dans une DLL atteint zéro, la DLL est déchargée de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a8b21-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="a8b21-114">**xlfRegister** (Formulaire 1) définit également un nom masqué qui est l'argument de texte de la fonction, _pxFunctionText_, et qui prend la valeur de l'ID d'enregistrement de la fonction ou de la commande.</span><span class="sxs-lookup"><span data-stu-id="a8b21-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="a8b21-115">Lors de l'annulation de l'inscription de la fonction, ce nom doit être supprimé à l'aide de **xlfSetName** afin que le nom de la fonction ne soit plus mentionné par l'Assistant fonction.</span><span class="sxs-lookup"><span data-stu-id="a8b21-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="a8b21-116">Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="a8b21-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="a8b21-117">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8b21-117">Parameters</span></span>

<span data-ttu-id="a8b21-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="a8b21-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="a8b21-119">ID d'inscription de la fonction dont l'inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="a8b21-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a8b21-120">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="a8b21-120">Property value/Return value</span></span>

<span data-ttu-id="a8b21-121">Si elle réussit, renvoie la **valeur true** (**xltypeBool**), sinon elle renvoie la valeur false.</span><span class="sxs-lookup"><span data-stu-id="a8b21-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8b21-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8b21-122">Remarks</span></span>

<span data-ttu-id="a8b21-123">L'ID d'inscription de la fonction est retourné par **xlfRegister** lorsque la fonction est inscrite pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="a8b21-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="a8b21-124">Elle peut également être obtenue en appelant la [fonction xlfRegisterId](xlfregisterid.md) ou la [fonction xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="a8b21-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="a8b21-125">Notez que xlfRegisterId essaie d'enregistrer la fonction si elle n'a pas encore été inscrite.</span><span class="sxs-lookup"><span data-stu-id="a8b21-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="a8b21-126">Pour cette raison, si vous tentez d'obtenir l'ID de sorte que vous puissiez annuler l'inscription de la fonction, il est préférable de l'obtenir en transmettant le nom enregistré à **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="a8b21-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="a8b21-127">Si la fonction n'a pas été enregistrée, **xlfEvaluate** échoue avec une #NAME? «.</span><span class="sxs-lookup"><span data-stu-id="a8b21-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a8b21-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8b21-128">Example</span></span>

<span data-ttu-id="a8b21-129">Voir le code de la fonction **fExit** dans `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="a8b21-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a><span data-ttu-id="a8b21-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8b21-130">See also</span></span>

- [<span data-ttu-id="a8b21-131">xlfRegister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="a8b21-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="a8b21-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="a8b21-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="a8b21-133">xlfUnregister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="a8b21-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="a8b21-134">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="a8b21-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

