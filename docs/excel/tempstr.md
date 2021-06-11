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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418042"
---
# <a name="tempstr"></a><span data-ttu-id="3a558-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="3a558-104">TempStr</span></span>

 <span data-ttu-id="3a558-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3a558-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3a558-106">Fonction de bibliothèque Deprecated Framework qui crée une **structure XLOPER** temporaire contenant une chaîne d’byte **xltypeStr.**</span><span class="sxs-lookup"><span data-stu-id="3a558-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="3a558-107">Il prend une chaîne source terminée par null comme entrée.</span><span class="sxs-lookup"><span data-stu-id="3a558-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="3a558-108">Il tente de faire ententer le premier caractère de la chaîne fournie par la longueur de la chaîne suivante.</span><span class="sxs-lookup"><span data-stu-id="3a558-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="3a558-109">Ce n’est pas toujours une chose sûre : Microsoft Excel risque de se crasher si une chaîne en lecture seule est transmise.</span><span class="sxs-lookup"><span data-stu-id="3a558-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="3a558-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a558-110">Parameters</span></span>

 <span data-ttu-id="3a558-111">_str_</span><span class="sxs-lookup"><span data-stu-id="3a558-111">_str_</span></span>
  
<span data-ttu-id="3a558-112">Pointeur vers la chaîne source terminée par null.</span><span class="sxs-lookup"><span data-stu-id="3a558-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="3a558-113">**TempStr** tronque les chaînes dont la durée est de plus de 255 octets.</span><span class="sxs-lookup"><span data-stu-id="3a558-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="3a558-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3a558-114">Return value</span></span>

<span data-ttu-id="3a558-115">Renvoie une **chaîne xltypeStr** contenant un pointeur vers la mémoire tampon de chaîne transmise.</span><span class="sxs-lookup"><span data-stu-id="3a558-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3a558-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a558-116">Remarks</span></span>

<span data-ttu-id="3a558-117">Cette façon de créer des chaînes temporaires est désormais dépréciée au profit de la façon dont [TempStrConst et TempStr12](tempstrconst-tempstr12.md) fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="3a558-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="3a558-118">Ces fonctions allouent une nouvelle mémoire tampon et y copient la chaîne transmise.</span><span class="sxs-lookup"><span data-stu-id="3a558-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="3a558-119">Les chaînes d’entrée **pour TempStrConst** et **TempStr12** ne sont pas modifiées et sont donc déclarées comme **const**.</span><span class="sxs-lookup"><span data-stu-id="3a558-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="3a558-120">En revanche, la chaîne d’entrée **à TempStr** est modifiée et ne peut donc pas être déclarée comme **const**.</span><span class="sxs-lookup"><span data-stu-id="3a558-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="3a558-121">Le premier caractère de la chaîne d’entrée est traité comme un espace pour un caractère de longueur et est remplacé par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3a558-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a558-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a558-122">See also</span></span>



[<span data-ttu-id="3a558-123">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="3a558-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

