---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- fonction xloper12toxloper [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422907"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="f559d-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="f559d-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="f559d-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f559d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f559d-106">Routine de conversion utilisée pour convertir à partir de la **nouvelle XLOPER12** vers l’ancienne **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="f559d-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="f559d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f559d-107">Parameters</span></span>

<span data-ttu-id="f559d-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="f559d-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="f559d-109">Pointeur vers la source **XLOPER12** à convertir.</span><span class="sxs-lookup"><span data-stu-id="f559d-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="f559d-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="f559d-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="f559d-111">Pointeur vers la **XLOPER cible** pour contenir la valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="f559d-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f559d-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="f559d-112">Property value/Return value</span></span>

<span data-ttu-id="f559d-113">**TRUE** si la conversion a réussi, FALSE dans **le** cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f559d-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f559d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f559d-114">Remarks</span></span>

<span data-ttu-id="f559d-115">Selon le type de **XLOPER12**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties, qui sont pointées vers la **XLOPER cible**.</span><span class="sxs-lookup"><span data-stu-id="f559d-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="f559d-116">L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est réussie . **FreeXLOperT peut être** utilisé, ou vous pouvez le faire directement à l’aide de **la gratuité.**</span><span class="sxs-lookup"><span data-stu-id="f559d-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="f559d-117">Si la conversion échoue, l’appelant n’a pas besoin de libérer de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f559d-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="f559d-118">La conversion d’une **xlOPER12** en **XLOPER** peut échouer lorsque la **XLOPER12** contient un tableau ou une référence trop grand ou une chaîne trop longue pour que la **XLOPER** contienne.</span><span class="sxs-lookup"><span data-stu-id="f559d-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="f559d-119">**XLOPER12** Les chaînes unicode à caractères larges sont converties en chaînes d’byte **XLOPER** ASCII d’une manière qui dépend des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="f559d-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="f559d-120">**XlOPER12** **xltypeInt** est un integer signé 32 bits, tandis que **xlOPER** **xltypeInt** est un integer signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f559d-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="f559d-121">Lorsqu’un nombre integer **XLOPER12** fourni dépasse la limite d’un nombre integer **XLOPER,** l’integer est converti en un double de 8 caractères et renvoyé dans une **XLOPER** de type **xltypeNum**.</span><span class="sxs-lookup"><span data-stu-id="f559d-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="f559d-122">Il s’agit du seul cas dans lequel cette fonction modifie le type de la **XLOPER convertie**.</span><span class="sxs-lookup"><span data-stu-id="f559d-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="f559d-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="f559d-123">Example</span></span>

<span data-ttu-id="f559d-124">Consultez le  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` fichier pour le code de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f559d-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f559d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f559d-125">See also</span></span>

- [<span data-ttu-id="f559d-126">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="f559d-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

