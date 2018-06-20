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
- fonction tempbool [excel 2007], fonction TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782192"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="98f3c-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="98f3c-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="98f3c-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98f3c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="98f3c-106">Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant la **valeur booléenne** **TRUE** ou **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="98f3c-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="98f3c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98f3c-107">Parameters</span></span>

 <span data-ttu-id="98f3c-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="98f3c-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="98f3c-109">Utilisez 0 pour renvoyer la **valeur FALSE**; utiliser une autre valeur pour renvoyer **la valeur TRUE**.</span><span class="sxs-lookup"><span data-stu-id="98f3c-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="98f3c-110">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="98f3c-110">Property value/Return value</span></span>

<span data-ttu-id="98f3c-111">Renvoie un **xltypeBool** **Boolean** contenant la valeur logique passée.</span><span class="sxs-lookup"><span data-stu-id="98f3c-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="98f3c-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="98f3c-112">Example</span></span>

<span data-ttu-id="98f3c-113">L’exemple suivant utilise la fonction **TempBool12** pour effacer la barre d’état.</span><span class="sxs-lookup"><span data-stu-id="98f3c-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="98f3c-114">Mémoire temporaire est libérée lorsque la fonction [Excel/Excel12f](excel-excel12f.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="98f3c-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="98f3c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98f3c-115">See also</span></span>



[<span data-ttu-id="98f3c-116">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="98f3c-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

