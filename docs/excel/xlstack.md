---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- fonction xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429978"
---
# <a name="xlstack"></a><span data-ttu-id="45f05-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="45f05-104">xlStack</span></span>

<span data-ttu-id="45f05-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="45f05-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="45f05-106">Vérifie la quantité d’espace laissé sur la pile.</span><span class="sxs-lookup"><span data-stu-id="45f05-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="45f05-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45f05-107">Parameters</span></span>

<span data-ttu-id="45f05-108">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="45f05-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="45f05-109">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="45f05-109">Property value/Return value</span></span>

<span data-ttu-id="45f05-110">Renvoie le nombre d’octets **(xltypeInt)** restants sur la pile.</span><span class="sxs-lookup"><span data-stu-id="45f05-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45f05-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="45f05-111">Remarks</span></span>

<span data-ttu-id="45f05-112">La quantité d’espace de pile disponible des versions récentes déborde de l’integer signé 16 bits de **la XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="45f05-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="45f05-113">Cela signifie que **xlStack** peut renvoyer une valeur entre -32767 et 32768 lorsqu’il est appelé à l’aide de **XLOPER** s et **Excel4** ou **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="45f05-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER** s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="45f05-114">Pour obtenir la valeur correcte dans ce cas, vous devez caster la valeur renvoyée en un raccourci non signé.</span><span class="sxs-lookup"><span data-stu-id="45f05-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="45f05-115">À partir de Excel 2007, vous devez appeler cette fonction à l’aide de **XLOPER12** s et **Excel12** ou **Excel12v**, auquel cas la valeur renvoyée est la quantité d’espace pile disponible ou 64 Ko, selon la valeur la plus faible.</span><span class="sxs-lookup"><span data-stu-id="45f05-115">Starting in Excel 2007, you should call this function using **XLOPER12** s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="45f05-116">Excel dispose d’une quantité limitée d’espace sur la pile et vous devez prendre soin de ne pas dépasser cet espace.</span><span class="sxs-lookup"><span data-stu-id="45f05-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="45f05-117">Ne placez jamais de très grandes structures de données sur la pile et faites autant de variables locales que possible statiques.</span><span class="sxs-lookup"><span data-stu-id="45f05-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="45f05-118">Évitez d’appeler des fonctions de manière récursive, car cela remplira rapidement la pile.</span><span class="sxs-lookup"><span data-stu-id="45f05-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="45f05-119">Si vous pensez que vous appelez cette fonction fréquemment pour voir la quantité d’espace de pile qui reste.</span><span class="sxs-lookup"><span data-stu-id="45f05-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="45f05-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="45f05-120">Example</span></span>

<span data-ttu-id="45f05-121">Le premier exemple affiche un message d’alerte contenant la quantité d’espace de pile gauche et est contenu dans  `\SAMPLES\EXAMPLE\EXAMPLE.C` .</span><span class="sxs-lookup"><span data-stu-id="45f05-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="45f05-122">Le deuxième exemple fait la même chose, en travaillant avec **xlOPER** et n’est pas contenu dans l’exemple de code SDK.</span><span class="sxs-lookup"><span data-stu-id="45f05-122">The second example does the same thing, working with **XLOPER** s and is not contained in the SDK example code.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="45f05-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45f05-123">See also</span></span>

- [<span data-ttu-id="45f05-124">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="45f05-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

