---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- fonction FuncFib [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310835"
---
# <a name="funcfib"></a><span data-ttu-id="a5bb7-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="a5bb7-104">FuncFib</span></span>

 <span data-ttu-id="a5bb7-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5bb7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5bb7-106">Exemple de fonction de feuille de calcul définie par l'utilisateur qui calcule le nième nombre de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="a5bb7-107">Lorsque GENERIC. xll est chargé, il enregistre cette fonction afin qu'elle puisse être appelée à partir de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="a5bb7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5bb7-108">Parameters</span></span>

 <span data-ttu-id="a5bb7-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a5bb7-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="a5bb7-110">Valeur de N pour laquelle le nième nombre de Fibonacci est requis.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a5bb7-111">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="a5bb7-111">Property value/Return value</span></span>

<span data-ttu-id="a5bb7-112">(**XLTYPENUM LPXLOPER12** en cas de réussite ou **xltypeErr** )</span><span class="sxs-lookup"><span data-stu-id="a5bb7-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="a5bb7-113">Nième nombre de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5bb7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5bb7-114">Remarks</span></span>

<span data-ttu-id="a5bb7-115">La fonction utilise une variable statique définie dans le bloc de fonction comme valeur de retour **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="a5bb7-116">Cette fonction n'est pas thread-safe et, par conséquent, cette fonction, ainsi que n'importe quelle fonction de feuille de calcul qui utilise cette stratégie pour renvoyer des **XLOPER**s ou **XLOPER12**, ne doit pas être inscrite en tant que thread-safe en commençant dans Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="a5bb7-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5bb7-117">Example</span></span>

<span data-ttu-id="a5bb7-118">Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5bb7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5bb7-119">See also</span></span>



[<span data-ttu-id="a5bb7-120">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="a5bb7-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

