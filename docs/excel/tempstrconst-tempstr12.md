---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- fonction tempstr12 [excel 2007], fonction TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782204"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="6a10c-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="6a10c-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="6a10c-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6a10c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6a10c-106">Fonction de bibliothèque Framework qui crée un temporaire **XLOPER/XLOPER12** qui contient une chaîne de **xltypeStr** , prenant une chaîne source se termine par null comme entrée.</span><span class="sxs-lookup"><span data-stu-id="6a10c-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="6a10c-107">La fonction alloue une nouvelle mémoire tampon et copie de la chaîne transmise dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="6a10c-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="6a10c-108">La chaîne d’entrée n’est pas modifiée et est donc déclarée comme **const**.</span><span class="sxs-lookup"><span data-stu-id="6a10c-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="6a10c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a10c-109">Parameters</span></span>

 <span data-ttu-id="6a10c-110">_Str_</span><span class="sxs-lookup"><span data-stu-id="6a10c-110">_str_</span></span>
  
<span data-ttu-id="6a10c-111">Pointeur vers la chaîne source terminée.</span><span class="sxs-lookup"><span data-stu-id="6a10c-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="6a10c-112">Dans le cas de **XLOPER**s, TempStrConst tronque les chaînes qui sont supérieures à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="6a10c-112">In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="6a10c-113">Dans le cas de **XLOPER12**s, TempStr12Const tronque les chaînes de longueur supérieure à 32 767 caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="6a10c-113">In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6a10c-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6a10c-114">Return value</span></span>

<span data-ttu-id="6a10c-115">Renvoie une chaîne **xltypeStr** contenant une copie de la mémoire tampon de chaîne transmise.</span><span class="sxs-lookup"><span data-stu-id="6a10c-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a10c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a10c-116">Remarks</span></span>

<span data-ttu-id="6a10c-117">Notez que la chaîne **XLOPER** fonction Framework, **TempStr**, se comporte différemment et tente de remplacer le premier caractère de la chaîne fournie avec la longueur de la chaîne suivante.</span><span class="sxs-lookup"><span data-stu-id="6a10c-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="6a10c-118">Ce n’est pas toujours une chose à faire fiable : Microsoft Excel peut s’interrompre si reçoit une chaîne en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a10c-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="6a10c-119">Cette méthode de création de chaînes temporaires est désormais déconseillée en faveur de celle dans laquelle le travail à la fois **TempStrConst** et **TempStr12** .</span><span class="sxs-lookup"><span data-stu-id="6a10c-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="6a10c-120">Par conséquent, le premier caractère de la chaîne d’entrée est traité comme point de départ de la chaîne, autrement dit, pas un caractère de longueur ou un espace pour un caractère de longueur.</span><span class="sxs-lookup"><span data-stu-id="6a10c-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="6a10c-121">Vous ne devez pas passer les chaînes qui ont un caractère de longueur codé au début, que les conséquences pourraient être imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="6a10c-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6a10c-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="6a10c-122">Example</span></span>

<span data-ttu-id="6a10c-123">Cet exemple utilise la fonction **TempStr12** pour créer une chaîne d’une zone de message.</span><span class="sxs-lookup"><span data-stu-id="6a10c-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6a10c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a10c-124">See also</span></span>



[<span data-ttu-id="6a10c-125">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="6a10c-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

