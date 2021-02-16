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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408914"
---
# <a name="func1"></a><span data-ttu-id="0ee79-104">Func1</span><span class="sxs-lookup"><span data-stu-id="0ee79-104">Func1</span></span>

 <span data-ttu-id="0ee79-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0ee79-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0ee79-106">L’exemple de fonction de feuille de calcul définie par l’utilisateur illustre le retour d’une valeur de chaîne statique.</span><span class="sxs-lookup"><span data-stu-id="0ee79-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="0ee79-107">Lorsque GENERIC.xll est chargé, il inscrit cette fonction afin qu’elle puisse être appelée à partir de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="0ee79-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="0ee79-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ee79-108">Parameters</span></span>

 <span data-ttu-id="0ee79-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="0ee79-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="0ee79-110">Cet argument est ignoré et sert uniquement à déclencher l’appel de la fonction par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0ee79-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0ee79-111">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="0ee79-111">Property value/Return value</span></span>

 <span data-ttu-id="0ee79-112">**LPXLOPER12**: toujours la chaîne « Func1 »</span><span class="sxs-lookup"><span data-stu-id="0ee79-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="0ee79-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ee79-113">Example</span></span>

<span data-ttu-id="0ee79-114">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="0ee79-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ee79-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ee79-115">See also</span></span>



[<span data-ttu-id="0ee79-116">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="0ee79-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

