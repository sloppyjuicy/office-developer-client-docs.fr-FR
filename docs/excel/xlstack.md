---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- fonction xlStack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782236"
---
# <a name="xlstack"></a><span data-ttu-id="e98de-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="e98de-104">xlStack</span></span>

<span data-ttu-id="e98de-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e98de-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e98de-106">Vérifie la quantité d’espace libre sur la pile.</span><span class="sxs-lookup"><span data-stu-id="e98de-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="e98de-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e98de-107">Parameters</span></span>

<span data-ttu-id="e98de-108">Cette fonction prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="e98de-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e98de-109">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e98de-109">Property value/Return value</span></span>

<span data-ttu-id="e98de-110">Renvoie le nombre d’octets (**xltypeInt**) restant sur la pile.</span><span class="sxs-lookup"><span data-stu-id="e98de-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e98de-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e98de-111">Remarks</span></span>

<span data-ttu-id="e98de-112">Nombre entier signé de 16 bits de la **XLOPER**de dépassement de la quantité d’espace de pile disponible des versions récentes.</span><span class="sxs-lookup"><span data-stu-id="e98de-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="e98de-113">Cela signifie que **xlStack** peut renvoyer une valeur entre-32767 et 32768 lorsqu’elle est appelée à l’aide de s **XLOPER**et **Excel4** ou **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="e98de-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER**s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="e98de-114">Pour obtenir la valeur correcte dans ce cas, vous devez effectuer un cast de la valeur renvoyée pour un court non signé.</span><span class="sxs-lookup"><span data-stu-id="e98de-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="e98de-115">À compter d’Excel 2007, vous devez appeler cette fonction à l’aide de s **XLOPER12**et **Excel12** ou **Excel12v**, auquel cas la valeur renvoyée est la quantité d’espace de pile ou de 64 Ko, selon ce qui est le plus petit.</span><span class="sxs-lookup"><span data-stu-id="e98de-115">Starting in Excel 2007, you should call this function using **XLOPER12**s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="e98de-116">Excel dispose de peu d’espace sur la pile, et vous devez veiller ne pas pour cet espace de saturation.</span><span class="sxs-lookup"><span data-stu-id="e98de-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="e98de-117">Ne jamais placer des structures de données très volumineuses sur la pile et rendre statiques variables autant que possible.</span><span class="sxs-lookup"><span data-stu-id="e98de-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="e98de-118">Éviter d’appeler des fonctions de manière récursive, car remplira rapidement la pile.</span><span class="sxs-lookup"><span data-stu-id="e98de-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="e98de-119">Si vous pensez que vous sont saturer la pile, appelez cette fonction fréquemment pour voir la quantité d’espace pile de gauche.</span><span class="sxs-lookup"><span data-stu-id="e98de-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="e98de-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="e98de-120">Example</span></span>

<span data-ttu-id="e98de-121">Le premier exemple affiche un message d’alerte contenant la quantité d’espace pile et se trouve dans `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="e98de-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="e98de-122">Le deuxième exemple effectue la même chose, utilisation de s **XLOPER**et ne figure pas dans l’exemple de code SDK.</span><span class="sxs-lookup"><span data-stu-id="e98de-122">The second example does the same thing, working with **XLOPER**s and is not contained in the SDK example code.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="e98de-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e98de-123">See also</span></span>

- [<span data-ttu-id="e98de-124">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="e98de-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

