---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- fonction func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782126"
---
# <a name="func1"></a><span data-ttu-id="08d4f-104">Func1</span><span class="sxs-lookup"><span data-stu-id="08d4f-104">Func1</span></span>

 <span data-ttu-id="08d4f-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="08d4f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="08d4f-106">Exemple de fonction définie par l’utilisateur la feuille de calcul illustre le retour d’une valeur de chaîne statique.</span><span class="sxs-lookup"><span data-stu-id="08d4f-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="08d4f-107">Lorsque GENERIC.xll est chargé, il enregistre cette fonction afin qu’elle peut être appelée à partir de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="08d4f-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="08d4f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08d4f-108">Parameters</span></span>

 <span data-ttu-id="08d4f-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="08d4f-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="08d4f-110">Cet argument est ignoré et sert uniquement à Microsoft Excel pour appeler la fonction de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="08d4f-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="08d4f-111">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="08d4f-111">Property value/Return value</span></span>

 <span data-ttu-id="08d4f-112">**LPXLOPER12**: toujours la chaîne « Func1 »</span><span class="sxs-lookup"><span data-stu-id="08d4f-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="08d4f-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="08d4f-113">Example</span></span>

<span data-ttu-id="08d4f-114">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="08d4f-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08d4f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08d4f-115">See also</span></span>



[<span data-ttu-id="08d4f-116">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="08d4f-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

