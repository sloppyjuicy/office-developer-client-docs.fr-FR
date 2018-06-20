---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- fonction funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782132"
---
# <a name="funcsum"></a><span data-ttu-id="f4425-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="f4425-104">FuncSum</span></span>

 <span data-ttu-id="f4425-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f4425-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f4425-106">Exemple de fonction définie par l’utilisateur la feuille de calcul qui accepte les arguments de 1 à 29 et calcule leur somme.</span><span class="sxs-lookup"><span data-stu-id="f4425-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="f4425-107">Chaque argument peut être un numéro unique, une plage ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="f4425-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="f4425-108">Lorsque GENERIC.xll est chargé, il enregistre cette fonction afin qu’elle peut être appelée à partir de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="f4425-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="f4425-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4425-109">Parameters</span></span>

 <span data-ttu-id="f4425-110">_PX1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="f4425-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="f4425-111">Pointeurs vers **XLOPER12** arguments.</span><span class="sxs-lookup"><span data-stu-id="f4425-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="f4425-112">La fonction accepte n’importe quel type de type d’entrée, mais codée uniquement pour fonctionner sur des nombres, tableaux littérales de numéros et plages contenant uniquement des nombres ou des cellules vides.</span><span class="sxs-lookup"><span data-stu-id="f4425-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="f4425-113">Si moins de 29 arguments sont fournis, les autres arguments sont fournis en tant que **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="f4425-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f4425-114">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f4425-114">Property value/Return value</span></span>

<span data-ttu-id="f4425-115">(**LPXLOPER12 xltypeNum** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="f4425-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="f4425-116">La somme des arguments ou #VALUE !</span><span class="sxs-lookup"><span data-stu-id="f4425-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="f4425-117">s’il y a les valeurs non numériques dans la liste d’arguments fournis ou d’une cellule dans une plage ou un élément dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="f4425-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="f4425-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="f4425-118">Example</span></span>

<span data-ttu-id="f4425-119">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f4425-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4425-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4425-120">See also</span></span>



[<span data-ttu-id="f4425-121">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="f4425-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

