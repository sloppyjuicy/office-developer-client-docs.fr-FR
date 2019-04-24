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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310352"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="bdcec-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="bdcec-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="bdcec-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bdcec-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bdcec-106">Fonction de bibliothèque d'infrastructure qui crée une expression **XLOPER**/ \*\*\*\* temporaire contenant la valeur **booléenne** **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="bdcec-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="bdcec-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdcec-107">Parameters</span></span>

 <span data-ttu-id="bdcec-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="bdcec-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="bdcec-109">Utilisez 0 pour renvoyer la **valeur false**; Utilisez n'importe quelle autre valeur pour renvoyer la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="bdcec-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bdcec-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="bdcec-110">Property value/Return value</span></span>

<span data-ttu-id="bdcec-111">Renvoie une valeur de **type Boolean** **xltypeBool** qui contient la valeur logique passée.</span><span class="sxs-lookup"><span data-stu-id="bdcec-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bdcec-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="bdcec-112">Example</span></span>

<span data-ttu-id="bdcec-113">L'exemple suivant utilise la fonction **TempBool12** pour effacer la barre d'État.</span><span class="sxs-lookup"><span data-stu-id="bdcec-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="bdcec-114">La mémoire temporaire est libérée lors de l'appel de la fonction [Excel/Excel12f](excel-excel12f.md) .</span><span class="sxs-lookup"><span data-stu-id="bdcec-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="bdcec-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdcec-115">See also</span></span>



[<span data-ttu-id="bdcec-116">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="bdcec-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

