---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- fonction xlGetHwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782241"
---
# <a name="xlgethwnd"></a><span data-ttu-id="55132-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="55132-104">xlGetHwnd</span></span>

<span data-ttu-id="55132-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55132-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="55132-106">Retourne le handle de fenêtre de la fenêtre Microsoft Excel de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="55132-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="55132-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55132-107">Parameters</span></span>

<span data-ttu-id="55132-108">Cette fonction ne comporte aucun argument.</span><span class="sxs-lookup"><span data-stu-id="55132-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="55132-109">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="55132-109">Property value/Return value</span></span>

<span data-ttu-id="55132-110">Contient le handle de fenêtre (**xltypeInt**) dans le champ **val.w** .</span><span class="sxs-lookup"><span data-stu-id="55132-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="55132-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="55132-111">Remarks</span></span>

<span data-ttu-id="55132-112">Cette fonction est utile pour l’écriture de code d’API Windows.</span><span class="sxs-lookup"><span data-stu-id="55132-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="55132-113">Lorsque vous appelez cette fonction à l’aide de [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), la variable de type entier XLOPER renvoyée est un entier signé 16 bits courte. Il s’agit des 16 bits de poids faibles de la poignée de Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="55132-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="55132-114">Pour trouver la partie haute, votre code doit itérer dans toutes les fenêtres ouvertes vous recherchez une correspondance avec la partie basse.</span><span class="sxs-lookup"><span data-stu-id="55132-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="55132-115">À compter d’Excel 2007, la variable de type entier de la **XLOPER12** est un int 32 bits signé et par conséquent contient le handle entier, évite d’avoir à parcourir toutes les fenêtres ouvertes.</span><span class="sxs-lookup"><span data-stu-id="55132-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="55132-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="55132-116">Example</span></span>

<span data-ttu-id="55132-117">Voir le code de la [fonction fShowDialog](fshowdialog.md) dans `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="55132-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55132-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55132-118">See also</span></span>

- [<span data-ttu-id="55132-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="55132-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="55132-120">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="55132-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

