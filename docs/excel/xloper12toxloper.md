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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782239"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="79ae3-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="79ae3-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="79ae3-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79ae3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="79ae3-106">Permet de convertir le nouveau **XLOPER12** l' ancienne **XLOPER**routine de conversion.</span><span class="sxs-lookup"><span data-stu-id="79ae3-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="79ae3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79ae3-107">Parameters</span></span>

<span data-ttu-id="79ae3-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="79ae3-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="79ae3-109">Pointeur vers la source **XLOPER12** à convertir.</span><span class="sxs-lookup"><span data-stu-id="79ae3-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="79ae3-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="79ae3-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="79ae3-111">Pointeur vers la cible **XLOPER** contenant la valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="79ae3-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="79ae3-112">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="79ae3-112">Property value/Return value</span></span>

<span data-ttu-id="79ae3-113">**TRUE** si la conversion a réussi, **FALSE** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="79ae3-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="79ae3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="79ae3-114">Remarks</span></span>

<span data-ttu-id="79ae3-115">Selon le type de la **XLOPER12**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties qui pointent sur la cible **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="79ae3-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="79ae3-116">L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est un succès ; **FreeXLOperT** peut être utilisé, ou elle peut être effectuée directement à l’aide de **libre**.</span><span class="sxs-lookup"><span data-stu-id="79ae3-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="79ae3-117">En cas d’échec de la conversion, l’appelant n’a pas besoin libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="79ae3-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="79ae3-118">Conversion d’un **XLOPER12** vers un **XLOPER** peut échouer lorsque le **XLOPER12** contient un tableau ou référence qui est trop grande ou une chaîne qui est trop longue pour le **XLOPER** contenir.</span><span class="sxs-lookup"><span data-stu-id="79ae3-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="79ae3-119">**XLOPER12** Chaînes de caractères larges Unicode sont convertis en chaînes d’octets ASCII **XLOPER** dans un façon dépendant des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="79ae3-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="79ae3-120">Le **XLOPER12** **xltypeInt** est un entier signé 32 bits, alors que le **XLOPER** **xltypeInt** est un nombre entier signé de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="79ae3-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="79ae3-121">Lorsqu’un entier **XLOPER12** fourni dépasse la limite d’un nombre entier **XLOPER** , l’entier est converti en un double de 8 octets et renvoyé dans un **XLOPER** de type **xltypeNum**.</span><span class="sxs-lookup"><span data-stu-id="79ae3-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="79ae3-122">Il s’agit du seul cas dans lequel cette fonction modifie le type de la convertie **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="79ae3-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="79ae3-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="79ae3-123">Example</span></span>

<span data-ttu-id="79ae3-124">Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="79ae3-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79ae3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79ae3-125">See also</span></span>

- [<span data-ttu-id="79ae3-126">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="79ae3-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

