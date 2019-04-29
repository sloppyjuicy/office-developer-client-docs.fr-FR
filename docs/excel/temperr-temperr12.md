---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- fonction tempérée [Excel 2007], fonction TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410608"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="9f201-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="9f201-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="9f201-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9f201-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9f201-106">Fonction de bibliothèque d'infrastructure qui crée une liste **XLOPER**/ \*\*\*\* temporaire contenant une erreur de feuille de calcul Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9f201-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="9f201-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f201-107">Parameters</span></span>

 <span data-ttu-id="9f201-108">_err_</span><span class="sxs-lookup"><span data-stu-id="9f201-108">_err_</span></span>
  
<span data-ttu-id="9f201-109">Le code d'erreur souhaité ou son équivalent numérique littéral, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9f201-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="9f201-110">**Error**</span><span class="sxs-lookup"><span data-stu-id="9f201-110">**Error**</span></span>|<span data-ttu-id="9f201-111">**Code d'erreur défini dans XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="9f201-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="9f201-112">**Équivalent décimal**</span><span class="sxs-lookup"><span data-stu-id="9f201-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f201-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="9f201-113">#NULL</span></span>  <br/> |<span data-ttu-id="9f201-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="9f201-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="9f201-115">0</span><span class="sxs-lookup"><span data-stu-id="9f201-115">0</span></span>  <br/> |
|<span data-ttu-id="9f201-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="9f201-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="9f201-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="9f201-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="9f201-118">7j/7</span><span class="sxs-lookup"><span data-stu-id="9f201-118">7</span></span>  <br/> |
|<span data-ttu-id="9f201-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="9f201-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="9f201-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="9f201-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="9f201-121">15 </span><span class="sxs-lookup"><span data-stu-id="9f201-121">15</span></span>  <br/> |
|<span data-ttu-id="9f201-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="9f201-122">#REF!</span></span>  <br/> |<span data-ttu-id="9f201-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="9f201-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="9f201-124">23</span><span class="sxs-lookup"><span data-stu-id="9f201-124">23</span></span>  <br/> |
|<span data-ttu-id="9f201-125">#NAME ?</span><span class="sxs-lookup"><span data-stu-id="9f201-125">#NAME?</span></span>  <br/> |<span data-ttu-id="9f201-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="9f201-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="9f201-127">29</span><span class="sxs-lookup"><span data-stu-id="9f201-127">29</span></span>  <br/> |
|<span data-ttu-id="9f201-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="9f201-128">#NUM!</span></span>  <br/> |<span data-ttu-id="9f201-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="9f201-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="9f201-130">36</span><span class="sxs-lookup"><span data-stu-id="9f201-130">36</span></span>  <br/> |
|<span data-ttu-id="9f201-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="9f201-131">#N/A</span></span>  <br/> |<span data-ttu-id="9f201-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="9f201-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="9f201-133">42</span><span class="sxs-lookup"><span data-stu-id="9f201-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="9f201-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9f201-134">Return value</span></span>

<span data-ttu-id="9f201-135">Renvoie un **xltypeBool** contenant le code d'erreur transmis.</span><span class="sxs-lookup"><span data-stu-id="9f201-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9f201-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="9f201-136">Example</span></span>

<span data-ttu-id="9f201-137">Cet exemple utilise la fonction **TempErr12** pour renvoyer une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="9f201-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="9f201-138">erreur à Excel.</span><span class="sxs-lookup"><span data-stu-id="9f201-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9f201-139">La fonction de bibliothèque d'infrastructure **TempErr12** alloue de la mémoire à partir d'une mémoire tampon interne, normalement libérée lors de l'appel de la fonction d'infrastructure **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="9f201-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="9f201-140">Si cet exemple de fonction est appelé à plusieurs reprises sans appel de **Excel12f** , une fuite de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="9f201-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="9f201-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f201-141">See also</span></span>



[<span data-ttu-id="9f201-142">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="9f201-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

