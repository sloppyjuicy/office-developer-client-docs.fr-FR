---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- fonction xlopertoxloper12 [excel 2007]
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
# <a name="xlopertoxloper12"></a><span data-ttu-id="a3673-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="a3673-104">XLOperToXLOper12</span></span>

<span data-ttu-id="a3673-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a3673-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a3673-106">Routine de conversion utilisée pour convertir de l’ancienne **XLOPER** vers la **nouvelle XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a3673-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="a3673-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3673-107">Parameters</span></span>

<span data-ttu-id="a3673-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="a3673-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="a3673-109">Pointeur vers la **XLOPER** source à convertir.</span><span class="sxs-lookup"><span data-stu-id="a3673-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="a3673-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a3673-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="a3673-111">Pointeur vers la **xlOPER12** cible pour contenir la valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="a3673-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a3673-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="a3673-112">Property value/Return value</span></span>

<span data-ttu-id="a3673-113">**TRUE** si la conversion a réussi, FALSE dans **le** cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a3673-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a3673-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3673-114">Remarks</span></span>

<span data-ttu-id="a3673-115">Selon le type de **XLOPER**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties, qui sont pointées vers la **xlOPER12 cible.**</span><span class="sxs-lookup"><span data-stu-id="a3673-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="a3673-116">L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est réussie . **FreeXLOper12T** peut être utilisé, ou vous pouvez le faire directement à l’aide **de la gratuité.**</span><span class="sxs-lookup"><span data-stu-id="a3673-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="a3673-117">Si la conversion échoue, l’appelant n’a pas besoin de libérer de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a3673-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="a3673-118">En règle générale, la conversion de **toute XLOPER** en **XLOPER12** est possible.</span><span class="sxs-lookup"><span data-stu-id="a3673-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="a3673-119">En revanche, la conversion d’une **xlOPER12** en **XLOPER** peut échouer lorsque la **XLOPER12** contient un tableau ou une référence trop grand ou une chaîne trop longue pour que la **XLOPER** contienne.</span><span class="sxs-lookup"><span data-stu-id="a3673-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="a3673-120">**XLOPER** Les chaînes d’byte ASCII sont converties en chaînes à caractères larges **XLOPER12** Unicode d’une manière qui dépend des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="a3673-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="a3673-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3673-121">Example</span></span>

<span data-ttu-id="a3673-122">Consultez le  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` fichier pour le code de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a3673-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

