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
- fonction Excel12v [excel 2007], fonction Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782128"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="2527f-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="2527f-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="2527f-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2527f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2527f-106">Appelle une fonction de feuille de calcul Microsoft Excel interne, la fonction de feuille macro ou commande, ou XLL seule fonction spéciale ou, à partir de DLL, XLL, ou de ressource de code.</span><span class="sxs-lookup"><span data-stu-id="2527f-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="2527f-107">Toutes les versions récentes d’Excel prennent en charge **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="2527f-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="2527f-108">À compter d’Excel 2007, **Excel12v** est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2527f-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="2527f-109">Ces fonctions peuvent être appelées uniquement lorsque Excel a réussi le contrôle à la DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="2527f-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="2527f-110">Ils peuvent également être appelées lorsque Excel a réussi le contrôle indirectement via un appel à Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="2527f-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="2527f-111">Ils ne peuvent pas être appelées à tout moment.</span><span class="sxs-lookup"><span data-stu-id="2527f-111">They cannot be called at any other time.</span></span> <span data-ttu-id="2527f-112">Par exemple, ils ne peuvent pas être appelées pendant un appel à la fonction DllMain ou autres heures lorsque le système d’exploitation a appelé la DLL ou d’un thread créé par la DLL.</span><span class="sxs-lookup"><span data-stu-id="2527f-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="2527f-113">Les fonctions [Excel 4 et Excel12](excel4-excel12.md) acceptent leurs arguments comme une liste de longueur variable sur la pile, tandis que les fonctions **Excel4v** et **Excel12v** acceptent que les arguments comme un tableau.</span><span class="sxs-lookup"><span data-stu-id="2527f-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="2527f-114">Dans tous les autres aspects **Excel4** se comporte comme **Excel4v**et **Excel12** se comporte comme **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="2527f-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="2527f-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2527f-115">Parameters</span></span>

 <span data-ttu-id="2527f-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="2527f-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="2527f-117">Un nombre qui indique la commande, une fonction ou une fonction spéciale que vous voulez appeler.</span><span class="sxs-lookup"><span data-stu-id="2527f-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="2527f-118">Pour obtenir la liste des valeurs valides _iFunction_ , voir la section Remarques suivante.</span><span class="sxs-lookup"><span data-stu-id="2527f-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="2527f-119">_pxRes_ (**LPXLOPER** ou **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="2527f-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="2527f-120">Pointeur vers un **XLOPER** (dans le cas d' **Excel4v**) ou une **XLOPER12** (dans le cas d' **Excel12v**) qui doit contenir le résultat de la fonction évaluée.</span><span class="sxs-lookup"><span data-stu-id="2527f-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="2527f-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="2527f-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="2527f-122">Le nombre d’arguments suivants qui seront transmises à la fonction.</span><span class="sxs-lookup"><span data-stu-id="2527f-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="2527f-123">Dans les versions d’Excel jusqu'à 2003 ce peut être n’importe quel nombre entre 0 et 30.</span><span class="sxs-lookup"><span data-stu-id="2527f-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="2527f-124">À compter d’Excel 2007, il peut être n’importe quel nombre compris entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="2527f-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="2527f-125">_rgx_ (**[De LPXLOPER]** ou **[] LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="2527f-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="2527f-126">Tableau qui contient les arguments de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2527f-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="2527f-127">Tous les arguments du tableau doivent être des pointeurs aux valeurs **XLOPER** ou **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="2527f-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="2527f-128">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2527f-128">Return value</span></span>

<span data-ttu-id="2527f-129">Ces fonctions renvoient les mêmes valeurs que **Excel4** et **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="2527f-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2527f-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="2527f-130">Remarks</span></span>

<span data-ttu-id="2527f-131">Ces fonctions sont utiles lorsque le nombre d’arguments transmis à l’opérateur est variable.</span><span class="sxs-lookup"><span data-stu-id="2527f-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="2527f-132">Par exemple, **Excel4v** et **Excel12v** sont utiles lorsque vous enregistrez des fonctions à l’aide de [xlfRegister](xlfregister-form-1.md) où le nombre d’arguments total dépend du nombre d’arguments effectuées par la fonction en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2527f-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="2527f-133">**Excel4v** et **Excel12v** sont également utiles lorsque vous écrivez une fonction wrapper pour **Excel4** ou **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="2527f-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="2527f-134">Dans ces cas-là, vous devez convertir une liste d’arguments variable, comme vous le feriez normalement être fournis à **Excel4** ou **Excel12**, à un argument de tableau unique de la taille de la variable de rappeler dans Excel à l’aide de **Excel4v** ou **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="2527f-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="2527f-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="2527f-135">Example</span></span>

<span data-ttu-id="2527f-136">Pour des exemples de code, voir le code pour les fonctions **Excel** et **Excel12f** dans le SDK XLL Excel 2010, à l’emplacement suivant, où vous avez installé le Kit de développement :</span><span class="sxs-lookup"><span data-stu-id="2527f-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="2527f-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="2527f-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2527f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2527f-138">See also</span></span>



[<span data-ttu-id="2527f-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="2527f-139">Excel4/Excel12</span></span>](excel4-excel12.md)

