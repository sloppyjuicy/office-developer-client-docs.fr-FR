---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- fonction Excel12v [Excel 2007], fonction Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310898"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="6584b-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="6584b-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="6584b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6584b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6584b-106">Appelle une fonction de feuille de calcul Microsoft Excel interne, une fonction de feuille de macro ou une commande, ou une fonction ou une commande spéciale XLL uniquement, à partir d'une ressource DLL, XLL ou de code.</span><span class="sxs-lookup"><span data-stu-id="6584b-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="6584b-107">Toutes les versions récentes d'Excel prennent en charge **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="6584b-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="6584b-108">À partir d'Excel 2007, **Excel12v** est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6584b-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="6584b-109">Ces fonctions ne peuvent être appelées que lorsqu'Excel a passé le contrôle à la DLL ou au XLL.</span><span class="sxs-lookup"><span data-stu-id="6584b-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="6584b-110">Elles peuvent également être appelées lorsqu'Excel a passé le contrôle indirectement via un appel à Visual Basic pour applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="6584b-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="6584b-111">Elles ne peuvent pas être appelées à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="6584b-111">They cannot be called at any other time.</span></span> <span data-ttu-id="6584b-112">Par exemple, ils ne peuvent pas être appelés pendant les appels à la fonction DllMain ou à d'autres moments où le système d'exploitation a appelé la DLL ou à partir d'un thread créé par la DLL.</span><span class="sxs-lookup"><span data-stu-id="6584b-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="6584b-113">Les fonctions [Excel4 et Excel12](excel4-excel12.md) acceptent leurs arguments sous la forme d'une liste de longueur variable dans la pile, tandis que les fonctions **Excel4v** et **Excel12v** acceptent leurs arguments sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="6584b-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="6584b-114">À tous les autres égards, **Excel4** se comporte de la même manière que **Excel4v**, et **Excel12** se comporte de la même manière que **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="6584b-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="6584b-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6584b-115">Parameters</span></span>

 <span data-ttu-id="6584b-116">_IFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="6584b-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="6584b-117">Nombre qui indique la commande, la fonction ou la fonction spéciale que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="6584b-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="6584b-118">Pour obtenir la liste des valeurs _IFunction_ valides, reportez-vous à la section notes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6584b-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="6584b-119">_pxRes_ (**LPXLOPER** ou **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="6584b-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="6584b-120">Pointeur vers une **XLOPER** (dans le cas de **Excel4v**) ou un **XLOPER12** (dans le cas de **Excel12v**) qui contiendra le résultat de la fonction évaluée.</span><span class="sxs-lookup"><span data-stu-id="6584b-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="6584b-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="6584b-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="6584b-122">Nombre d'arguments suivants qui seront transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="6584b-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="6584b-123">Dans les versions d'Excel jusqu'à 2003, il peut s'agir d'un nombre compris entre 0 et 30.</span><span class="sxs-lookup"><span data-stu-id="6584b-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="6584b-124">À partir d'Excel 2007, il peut s'agir de n'importe quel nombre compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="6584b-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="6584b-125">_RGX_ (**LPXLOPER []** ou **LPXLOPER12 []**)</span><span class="sxs-lookup"><span data-stu-id="6584b-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="6584b-126">Tableau qui contient les arguments de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6584b-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="6584b-127">Tous les arguments dans le tableau doivent être des pointeurs vers les valeurs **XLOPER** ou **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="6584b-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="6584b-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6584b-128">Return value</span></span>

<span data-ttu-id="6584b-129">Ces fonctions renvoient les mêmes valeurs que **Excel4** et **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="6584b-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6584b-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="6584b-130">Remarks</span></span>

<span data-ttu-id="6584b-131">Ces fonctions sont utiles lorsque le nombre d'arguments transmis à l'opérateur est variable.</span><span class="sxs-lookup"><span data-stu-id="6584b-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="6584b-132">Par exemple, **Excel4v** et **Excel12v** sont utiles lorsque vous enregistrez des fonctions à l'aide de [xlfRegister](xlfregister-form-1.md) , où le nombre d'arguments total dépend du nombre d'arguments pris par la fonction en cours d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6584b-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="6584b-133">**Excel4v** et **Excel12v** sont également utiles lorsque vous écrivez une fonction de wrapper pour **Excel4** ou **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="6584b-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="6584b-134">Dans ce cas, vous devez convertir une liste d'arguments de variable, comme normalement fourni à **Excel4** ou **Excel12**, à un seul argument de tableau de taille variable pour rappeler dans Excel à l'aide de **Excel4v** ou de **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="6584b-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="6584b-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="6584b-135">Example</span></span>

<span data-ttu-id="6584b-136">Pour des exemples de code, reportez-vous au code pour les fonctions **Excel** et **EXCEL12F** dans le kit de développement XLL Excel 2010, à l'emplacement suivant où vous avez installé le kit de développement logiciel (SDK):</span><span class="sxs-lookup"><span data-stu-id="6584b-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="6584b-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="6584b-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6584b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6584b-138">See also</span></span>



[<span data-ttu-id="6584b-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="6584b-139">Excel4/Excel12</span></span>](excel4-excel12.md)

