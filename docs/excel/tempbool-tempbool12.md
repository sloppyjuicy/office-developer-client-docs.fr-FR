---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- fonction tempbool [Excel 2007], fonction TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433716"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="39972-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="39972-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="39972-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="39972-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="39972-106">Fonction de bibliothèque d'infrastructure qui crée une expression **XLOPER**/ \*\*\*\* temporaire contenant la valeur **booléenne** **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="39972-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="39972-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39972-107">Parameters</span></span>

 <span data-ttu-id="39972-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="39972-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="39972-109">Utilisez 0 pour renvoyer la **valeur false**; Utilisez n'importe quelle autre valeur pour renvoyer la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="39972-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="39972-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="39972-110">Property value/Return value</span></span>

<span data-ttu-id="39972-111">Renvoie une valeur de **type Boolean** **xltypeBool** qui contient la valeur logique passée.</span><span class="sxs-lookup"><span data-stu-id="39972-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="39972-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="39972-112">Example</span></span>

<span data-ttu-id="39972-113">L'exemple suivant utilise la fonction **TempBool12** pour effacer la barre d'État.</span><span class="sxs-lookup"><span data-stu-id="39972-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="39972-114">La mémoire temporaire est libérée lors de l'appel de la fonction [Excel/Excel12f](excel-excel12f.md) .</span><span class="sxs-lookup"><span data-stu-id="39972-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="39972-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39972-115">See also</span></span>



[<span data-ttu-id="39972-116">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="39972-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

