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
- fonction temperr [excel 2007], fonction TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782189"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="7cf78-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="7cf78-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="7cf78-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7cf78-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7cf78-106">Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant une erreur de feuille de calcul Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7cf78-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="7cf78-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cf78-107">Parameters</span></span>

 <span data-ttu-id="7cf78-108">_message d’erreur_</span><span class="sxs-lookup"><span data-stu-id="7cf78-108">_err_</span></span>
  
<span data-ttu-id="7cf78-109">Le code d’erreur de votre choix, ou son équivalent numérique littérale, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7cf78-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="7cf78-110">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="7cf78-110">**Error**</span></span>|<span data-ttu-id="7cf78-111">**Code d’erreur défini dans XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="7cf78-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="7cf78-112">**Équivalent décimal**</span><span class="sxs-lookup"><span data-stu-id="7cf78-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cf78-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="7cf78-113">#NULL</span></span>  <br/> |<span data-ttu-id="7cf78-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="7cf78-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="7cf78-115">0</span><span class="sxs-lookup"><span data-stu-id="7cf78-115">0</span></span>  <br/> |
|<span data-ttu-id="7cf78-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="7cf78-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="7cf78-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="7cf78-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="7cf78-118">7</span><span class="sxs-lookup"><span data-stu-id="7cf78-118">7</span></span>  <br/> |
|<span data-ttu-id="7cf78-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="7cf78-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="7cf78-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="7cf78-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="7cf78-121">15</span><span class="sxs-lookup"><span data-stu-id="7cf78-121">15</span></span>  <br/> |
|<span data-ttu-id="7cf78-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="7cf78-122">#REF!</span></span>  <br/> |<span data-ttu-id="7cf78-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="7cf78-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="7cf78-124">23</span><span class="sxs-lookup"><span data-stu-id="7cf78-124">23</span></span>  <br/> |
|<span data-ttu-id="7cf78-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="7cf78-125">#NAME?</span></span>  <br/> |<span data-ttu-id="7cf78-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="7cf78-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="7cf78-127">29</span><span class="sxs-lookup"><span data-stu-id="7cf78-127">29</span></span>  <br/> |
|<span data-ttu-id="7cf78-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="7cf78-128">#NUM!</span></span>  <br/> |<span data-ttu-id="7cf78-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="7cf78-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="7cf78-130">36</span><span class="sxs-lookup"><span data-stu-id="7cf78-130">36</span></span>  <br/> |
|<span data-ttu-id="7cf78-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="7cf78-131">#N/A</span></span>  <br/> |<span data-ttu-id="7cf78-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="7cf78-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="7cf78-133">42</span><span class="sxs-lookup"><span data-stu-id="7cf78-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="7cf78-134">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7cf78-134">Return value</span></span>

<span data-ttu-id="7cf78-135">Renvoie une **xltypeBool** contenant le code d’erreur passé.</span><span class="sxs-lookup"><span data-stu-id="7cf78-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7cf78-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="7cf78-136">Example</span></span>

<span data-ttu-id="7cf78-137">Cet exemple utilise la fonction **TempErr12** pour renvoyer un #VALUE !</span><span class="sxs-lookup"><span data-stu-id="7cf78-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="7cf78-138">erreur Excel.</span><span class="sxs-lookup"><span data-stu-id="7cf78-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7cf78-139">La fonction de bibliothèque Framework **TempErr12** alloue de la mémoire d’un tampon interne, qui est libéré normalement lorsque la fonction de la structure **Excel12f** est appelée.</span><span class="sxs-lookup"><span data-stu-id="7cf78-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="7cf78-140">Si cet exemple de fonction est appelé à plusieurs reprises sans **Excel12f** appelée, une fuite de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="7cf78-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="7cf78-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cf78-141">See also</span></span>



[<span data-ttu-id="7cf78-142">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="7cf78-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

