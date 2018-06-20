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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782254"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="fb434-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="fb434-104">XLOperToXLOper12</span></span>

<span data-ttu-id="fb434-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb434-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fb434-106">Routine de conversion utilisée pour convertir l' ancien **XLOPER** vers le nouveau **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="fb434-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="fb434-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb434-107">Parameters</span></span>

<span data-ttu-id="fb434-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="fb434-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="fb434-109">Pointeur vers la source **XLOPER** à convertir.</span><span class="sxs-lookup"><span data-stu-id="fb434-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="fb434-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="fb434-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="fb434-111">Pointeur vers la cible **XLOPER12** contenant la valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="fb434-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fb434-112">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fb434-112">Property value/Return value</span></span>

<span data-ttu-id="fb434-113">**TRUE** si la conversion a réussi, **FALSE** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fb434-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fb434-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb434-114">Remarks</span></span>

<span data-ttu-id="fb434-115">Selon le type de l' **élément XLOPER**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties qui pointent sur la cible **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="fb434-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="fb434-116">L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est un succès ; **FreeXLOper12T** peut être utilisé, ou elle peut être effectuée directement à l’aide **disponible**.</span><span class="sxs-lookup"><span data-stu-id="fb434-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="fb434-117">En cas d’échec de la conversion, l’appelant n’a pas besoin libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="fb434-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="fb434-118">En règle générale, la conversion à partir de n’importe quel **XLOPER** un **XLOPER12** est possible.</span><span class="sxs-lookup"><span data-stu-id="fb434-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="fb434-119">En revanche, conversion d’un **XLOPER12** vers un **XLOPER** peut échouer lorsque le **XLOPER12** contient un tableau ou référence qui est trop grande ou une chaîne qui est trop longue pour le **XLOPER** contenir.</span><span class="sxs-lookup"><span data-stu-id="fb434-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="fb434-120">**XLOPER** Chaînes d’octets ASCII sont convertis en chaînes de caractères larges **XLOPER12** Unicode d’une manière qui dépend des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="fb434-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="fb434-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="fb434-121">Example</span></span>

<span data-ttu-id="fb434-122">Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="fb434-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

