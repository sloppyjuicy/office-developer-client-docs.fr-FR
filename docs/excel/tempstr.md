---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- fonction tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782201"
---
# <a name="tempstr"></a><span data-ttu-id="3a868-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="3a868-104">TempStr</span></span>

 <span data-ttu-id="3a868-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3a868-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3a868-106">Obsolète fonction bibliothèque Framework qui crée un temporaire **XLOPER** contenant une chaîne d’octets **xltypeStr** .</span><span class="sxs-lookup"><span data-stu-id="3a868-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="3a868-107">Il prend une chaîne source se termine par null comme entrée.</span><span class="sxs-lookup"><span data-stu-id="3a868-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="3a868-108">Il essaie de remplacer le premier caractère de la chaîne fournie avec la longueur de la chaîne suivante.</span><span class="sxs-lookup"><span data-stu-id="3a868-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="3a868-109">Ce n’est pas toujours une chose à faire fiable : Microsoft Excel peut s’interrompre si reçoit une chaîne en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3a868-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="3a868-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a868-110">Parameters</span></span>

 <span data-ttu-id="3a868-111">_Str_</span><span class="sxs-lookup"><span data-stu-id="3a868-111">_str_</span></span>
  
<span data-ttu-id="3a868-112">Pointeur vers la chaîne source terminée.</span><span class="sxs-lookup"><span data-stu-id="3a868-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="3a868-113">**TempStr** tronque les chaînes qui sont supérieures à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="3a868-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="3a868-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3a868-114">Return value</span></span>

<span data-ttu-id="3a868-115">Renvoie une chaîne **xltypeStr** contenant un pointeur vers la mémoire tampon de chaîne transmise.</span><span class="sxs-lookup"><span data-stu-id="3a868-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3a868-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a868-116">Remarks</span></span>

<span data-ttu-id="3a868-117">Cette méthode de création de chaînes temporaires est désormais déconseillée en faveur de la façon dans les deux [TempStrConst et TempStr12](tempstrconst-tempstr12.md) de travail.</span><span class="sxs-lookup"><span data-stu-id="3a868-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="3a868-118">Ces fonctions allouer une nouvelle mémoire tampon et copiez la chaîne transmise.</span><span class="sxs-lookup"><span data-stu-id="3a868-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="3a868-119">Les chaînes d’entrée pour **TempStrConst** et **TempStr12** ne sont pas modifiées et sont donc déclarés comme **const**.</span><span class="sxs-lookup"><span data-stu-id="3a868-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="3a868-120">En revanche, la chaîne d’entrée **TempStr** est modifiée et donc ne peut pas être déclarée comme **const**.</span><span class="sxs-lookup"><span data-stu-id="3a868-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="3a868-121">Le premier caractère de la chaîne d’entrée est traité comme un espace pour un caractère de longueur et est remplacé par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3a868-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a868-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a868-122">See also</span></span>



[<span data-ttu-id="3a868-123">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="3a868-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

