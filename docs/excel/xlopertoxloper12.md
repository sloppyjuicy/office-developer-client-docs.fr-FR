---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- fonction xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404595"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="d2144-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="d2144-104">XLOperToXLOper12</span></span>

<span data-ttu-id="d2144-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d2144-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d2144-106">Routine de conversion utilisée pour convertir une ancienne forme **XLOPER** en une nouvelle **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="d2144-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="d2144-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2144-107">Parameters</span></span>

<span data-ttu-id="d2144-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="d2144-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="d2144-109">Pointeur vers le **XLOPER** source à convertir.</span><span class="sxs-lookup"><span data-stu-id="d2144-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="d2144-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="d2144-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="d2144-111">Pointeur vers la cible **XLOPER12** cible pour contenir la valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="d2144-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d2144-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="d2144-112">Property value/Return value</span></span>

<span data-ttu-id="d2144-113">**True** si la conversion a réussi \*\*\*\* , false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d2144-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2144-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2144-114">Remarks</span></span>

<span data-ttu-id="d2144-115">Selon le type de l' **XLOPER**, cette fonction alloue une nouvelle mémoire tampon de mémoire pour les valeurs converties, qui sont pointées dans le **XLOPER12**cible.</span><span class="sxs-lookup"><span data-stu-id="d2144-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="d2144-116">L'appelant est chargé de libérer de la mémoire associée à la copie si la conversion a réussi; **FreeXLOper12T** peut être utilisé ou peut être réalisé directement à l'aide de **Free**.</span><span class="sxs-lookup"><span data-stu-id="d2144-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="d2144-117">Si la conversion échoue, l'appelant n'a pas besoin de libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d2144-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="d2144-118">En règle générale, la conversion d'une structure **XLOPER** en une expression **XLOPER12** est possible.</span><span class="sxs-lookup"><span data-stu-id="d2144-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="d2144-119">En revanche, la conversion d'un **XLOPER12** en une structure **XLOPER** peut échouer lorsque la variable **XLOPER12** contient un tableau ou une référence trop grande ou une chaîne trop longue pour l' **XLOPER** à contenir.</span><span class="sxs-lookup"><span data-stu-id="d2144-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="d2144-120">**XLOPER** Les chaînes d'octets ASCII sont \*\*\*\* converties en chaînes de caractères larges Unicode et conformes aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d2144-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="d2144-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2144-121">Example</span></span>

<span data-ttu-id="d2144-122">Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d2144-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

