---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- fonction XLOper12ToXLOper [Excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310072"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="f7e6a-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="f7e6a-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="f7e6a-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7e6a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f7e6a-106">Routine de conversion utilisée pour convertir la nouvelle **XLOPER12** en l'ancien **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="f7e6a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7e6a-107">Parameters</span></span>

<span data-ttu-id="f7e6a-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="f7e6a-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="f7e6a-109">Pointeur vers la source **XLOPER12** à convertir.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="f7e6a-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="f7e6a-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="f7e6a-111">Pointeur vers le **XLOPER** cible pour contenir la valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f7e6a-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="f7e6a-112">Property value/Return value</span></span>

<span data-ttu-id="f7e6a-113">**True** si la conversion a réussi \*\*\*\* , false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f7e6a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7e6a-114">Remarks</span></span>

<span data-ttu-id="f7e6a-115">Selon le type de **XLOPER12**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties, qui sont pointées dans le **XLOPER**cible.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="f7e6a-116">L'appelant est chargé de libérer de la mémoire associée à la copie si la conversion a réussi; **FreeXLOperT** peut être utilisé ou peut être réalisé directement à l'aide de la version **gratuite**.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="f7e6a-117">Si la conversion échoue, l'appelant n'a pas besoin de libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="f7e6a-118">La conversion d'un **XLOPER12** en une structure **XLOPER** peut échouer lorsque la variable **XLOPER12** contient un tableau ou une référence trop grande ou une chaîne trop longue pour l' **XLOPER** à contenir.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="f7e6a-119">**XLOPER12** Les chaînes de caractères larges Unicode sont converties en chaînes d'octets **XLOPER** ASCII d'une façon qui dépend des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="f7e6a-120">La \*\*\*\* **xltypeInt** XLOPER12 est un entier signé de 32 bits, tandis que le **XLOPER** **xltypeInt** est un entier signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="f7e6a-121">Lorsqu'un entier **XLOPER12** fourni dépasse la limite d'un entier **XLOPER** , l'entier est converti en double de 8 octets et renvoyé dans un **XLOPER** de type **xltypeNum**.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="f7e6a-122">Il s'agit du seul cas où cette fonction modifie le type de l' **XLOPER**converti.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="f7e6a-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="f7e6a-123">Example</span></span>

<span data-ttu-id="f7e6a-124">Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f7e6a-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7e6a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7e6a-125">See also</span></span>

- [<span data-ttu-id="f7e6a-126">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="f7e6a-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

