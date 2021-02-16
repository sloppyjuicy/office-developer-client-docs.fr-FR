---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- fonction xlgethwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425455"
---
# <a name="xlgethwnd"></a><span data-ttu-id="90641-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="90641-104">xlGetHwnd</span></span>

<span data-ttu-id="90641-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="90641-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="90641-106">Renvoie le handle de fenêtre de la fenêtre Microsoft Excel de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="90641-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="90641-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90641-107">Parameters</span></span>

<span data-ttu-id="90641-108">Cette fonction n’a pas d’arguments.</span><span class="sxs-lookup"><span data-stu-id="90641-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="90641-109">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="90641-109">Property value/Return value</span></span>

<span data-ttu-id="90641-110">Contient le handle de fenêtre (**xltypeInt**) dans le **champ val.w.**</span><span class="sxs-lookup"><span data-stu-id="90641-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90641-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="90641-111">Remarks</span></span>

<span data-ttu-id="90641-112">Cette fonction est utile pour écrire du code d’API Windows.</span><span class="sxs-lookup"><span data-stu-id="90641-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="90641-113">Lorsque vous appelez cette fonction à l’aide [d’Excel4](excel4-excel12.md) ou [d’Excel4v,](excel4v-excel12v.md)la variable d’integer XLOPER renvoyée est un int court signé 16 bits. Cette capacité ne peut contenir que les 16 bits faibles du handle Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="90641-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="90641-114">Pour trouver la partie la plus élevée, votre code doit itérer dans toutes les fenêtres ouvertes à la recherche d’une correspondance avec la partie basse.</span><span class="sxs-lookup"><span data-stu-id="90641-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="90641-115">À compter d’Excel 2007, la variable entière de la **xlOPER12** est un entier signé 32 bits et contient donc la poignée entière, ce qui supprime la nécessité d’itérer toutes les fenêtres ouvertes.</span><span class="sxs-lookup"><span data-stu-id="90641-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="90641-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="90641-116">Example</span></span>

<span data-ttu-id="90641-117">Consultez le code de la [fonction fShowDialog dans](fshowdialog.md)  `SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="90641-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90641-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90641-118">See also</span></span>

- [<span data-ttu-id="90641-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="90641-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="90641-120">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="90641-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

