---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- fonction funcfib [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782124"
---
# <a name="funcfib"></a><span data-ttu-id="70b6f-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="70b6f-104">FuncFib</span></span>

 <span data-ttu-id="70b6f-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="70b6f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="70b6f-106">Exemple de fonction définie par l’utilisateur la feuille de calcul qui calcule le nombre Fibonacci nième.</span><span class="sxs-lookup"><span data-stu-id="70b6f-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="70b6f-107">Lorsque GENERIC.xll est chargé, il enregistre cette fonction afin qu’elle peut être appelée à partir de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="70b6f-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="70b6f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70b6f-108">Parameters</span></span>

 <span data-ttu-id="70b6f-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="70b6f-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="70b6f-110">La valeur de N pour lequel le nombre de Fibonacci nième est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="70b6f-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="70b6f-111">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="70b6f-111">Property value/Return value</span></span>

<span data-ttu-id="70b6f-112">(**xltypeNum LPXLOPER12** en cas de réussite ou **xltypeErr** dans le cas contraire)</span><span class="sxs-lookup"><span data-stu-id="70b6f-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="70b6f-113">Le nombre de Fibonacci nième.</span><span class="sxs-lookup"><span data-stu-id="70b6f-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70b6f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="70b6f-114">Remarks</span></span>

<span data-ttu-id="70b6f-115">La fonction utilise une variable statique définie dans le bloc de fonction comme valeur de retour **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="70b6f-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="70b6f-116">Ce n’est pas thread-safe, et cette fonction et une fonction de feuille de calcul qui utilise cette stratégie pour le renvoi **XLOPER**ou **XLOPER12**, ne doivent pas être enregistrées en tant que thread-safe à compter d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="70b6f-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="70b6f-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="70b6f-117">Example</span></span>

<span data-ttu-id="70b6f-118">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="70b6f-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70b6f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70b6f-119">See also</span></span>



[<span data-ttu-id="70b6f-120">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="70b6f-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

