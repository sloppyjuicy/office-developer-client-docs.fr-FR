---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- fonction xlStack [Excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310156"
---
# <a name="xlstack"></a><span data-ttu-id="5ad8c-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="5ad8c-104">xlStack</span></span>

<span data-ttu-id="5ad8c-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5ad8c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5ad8c-106">Vérifie la quantité d'espace restant sur la pile.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="5ad8c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ad8c-107">Parameters</span></span>

<span data-ttu-id="5ad8c-108">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5ad8c-109">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="5ad8c-109">Property value/Return value</span></span>

<span data-ttu-id="5ad8c-110">Renvoie le nombre d'octets (**xltypeInt**) restants sur la pile.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ad8c-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ad8c-111">Remarks</span></span>

<span data-ttu-id="5ad8c-112">La quantité d'espace de pile disponible des versions récentes déborde de l'entier signé 16 bits de **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="5ad8c-113">Cela signifie que **xlStack** peut renvoyer une valeur comprise entre-32767 et 32768 lorsqu'il est appelé à l'aide de **XLOPER**s et **Excel4** ou **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER**s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="5ad8c-114">Pour obtenir la valeur correcte dans ce cas, vous devez effectuer un cast de la valeur renvoyée en un type unsigned short.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="5ad8c-115">À partir d'Excel 2007, vous devez appeler cette fonction à l'aide de **XLOPER12**s et **Excel12** ou **Excel12v**, auquel cas la valeur renvoyée est la quantité d'espace de pile disponible ou 64 Ko, la valeur la plus faible étant retenue.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-115">Starting in Excel 2007, you should call this function using **XLOPER12**s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="5ad8c-116">Excel dispose d'un espace limité sur la pile et vous devez veiller à ne pas saturer cet espace.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="5ad8c-117">Ne jamais placer de très grandes structures de données sur la pile et définir autant de variables locales que possible.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="5ad8c-118">Évitez d'appeler des fonctions de manière récursive, car cela remplira rapidement la pile.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="5ad8c-119">Si vous pensez que vous avez le temps de relancer la pile, appelez fréquemment cette fonction pour voir la taille de l'espace de pile restant.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="5ad8c-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="5ad8c-120">Example</span></span>

<span data-ttu-id="5ad8c-121">Le premier exemple affiche un message d'alerte contenant la quantité d'espace de pile à gauche et `\SAMPLES\EXAMPLE\EXAMPLE.C`est contenu dans.</span><span class="sxs-lookup"><span data-stu-id="5ad8c-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="5ad8c-122">Le deuxième exemple effectue la même chose, en travaillant avec **XLOPER**s et n'est pas inclus dans l'exemple de code du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="5ad8c-122">The second example does the same thing, working with **XLOPER**s and is not contained in the SDK example code.</span></span>
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="5ad8c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ad8c-123">See also</span></span>

- [<span data-ttu-id="5ad8c-124">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="5ad8c-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

