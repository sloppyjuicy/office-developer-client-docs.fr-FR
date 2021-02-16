---
title: xlfUnregister (formulaire 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- fonction xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410083"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="26e77-104">xlfUnregister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="26e77-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="26e77-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="26e77-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="26e77-106">Peut être appelée à partir d’une commande DLL ou XLL qui a elle-même été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="26e77-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="26e77-107">Cela équivaut à appeler **UNREGISTER à** partir d’une feuille macro XLM Excel.</span><span class="sxs-lookup"><span data-stu-id="26e77-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="26e77-108">**xlfUnregister** peut être appelé sous deux formes :</span><span class="sxs-lookup"><span data-stu-id="26e77-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="26e77-109">Formulaire 1 : désinsère une commande ou une fonction individuelle.</span><span class="sxs-lookup"><span data-stu-id="26e77-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="26e77-110">Formulaire 2 : décharge et désactive une XLL.</span><span class="sxs-lookup"><span data-stu-id="26e77-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="26e77-111">Appelée dans le formulaire 1, cette fonction réduit le nombre d’utilisations d’une fonction ou d’une commande DLL précédemment inscrite à l’aide de **xlfRegister** ou **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="26e77-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="26e77-112">Si le nombre d’utilisations est déjà zéro, cette fonction n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="26e77-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="26e77-113">Lorsque le nombre d’utilisations de toutes les fonctions dans une DLL atteint zéro, la DLL est déchargée de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="26e77-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="26e77-114">**xlfRegister** (formulaire 1) définit également un nom masqué qui est l’argument de texte de la fonction,  _pxFunctionText_, et qui est évalué en fonction de l’ID d’inscription de la fonction ou de la commande.</span><span class="sxs-lookup"><span data-stu-id="26e77-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="26e77-115">Lors de la désinssion de la fonction, ce nom doit être supprimé à l’aide de **xlfSetName** afin que le nom de la fonction ne soit plus répertorié par l’Assistant Fonction.</span><span class="sxs-lookup"><span data-stu-id="26e77-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="26e77-116">Pour plus d’informations, reportez-vous à la rubrique [Problèmes connus concernant le développement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="26e77-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="26e77-117">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26e77-117">Parameters</span></span>

<span data-ttu-id="26e77-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="26e77-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="26e77-119">ID d’inscription de la fonction à désinsister.</span><span class="sxs-lookup"><span data-stu-id="26e77-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="26e77-120">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="26e77-120">Property value/Return value</span></span>

<span data-ttu-id="26e77-121">Si elle réussit, renvoie **TRUE** (**xltypeBool**), sinon elle renvoie FALSE.</span><span class="sxs-lookup"><span data-stu-id="26e77-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26e77-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="26e77-122">Remarks</span></span>

<span data-ttu-id="26e77-123">L’ID d’inscription de la fonction est renvoyé par **xlfRegister** lors de la première inscription de la fonction.</span><span class="sxs-lookup"><span data-stu-id="26e77-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="26e77-124">Il peut également être obtenu en appelant la fonction [xlfRegisterId](xlfregisterid.md) ou [la fonction xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="26e77-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="26e77-125">Notez que xlfRegisterId tente d’inscrire la fonction si elle n’a pas déjà été inscrite.</span><span class="sxs-lookup"><span data-stu-id="26e77-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="26e77-126">Pour cette raison, si vous essayez uniquement d’obtenir l’ID afin de pouvoir désinsérer la fonction, il est préférable de l’obtenir en passant le nom enregistré à **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="26e77-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="26e77-127">Si la fonction n’a pas été enregistrée, **xlfEvaluate** échoue avec une #NAME ? erreur.</span><span class="sxs-lookup"><span data-stu-id="26e77-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="26e77-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="26e77-128">Example</span></span>

<span data-ttu-id="26e77-129">Consultez le code de la **fonction fExit** dans  `\SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="26e77-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="26e77-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26e77-130">See also</span></span>

- [<span data-ttu-id="26e77-131">xlfRegister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="26e77-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="26e77-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="26e77-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="26e77-133">xlfUnregister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="26e77-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="26e77-134">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="26e77-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

