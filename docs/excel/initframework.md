---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- fonction InitFramework [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420752"
---
# <a name="initframework"></a><span data-ttu-id="50d89-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="50d89-104">InitFramework</span></span>

 <span data-ttu-id="50d89-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="50d89-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="50d89-106">Fonction de bibliothèque d'infrastructure qui initialise la bibliothèque d'infrastructure, qui initialise simplement les structures de données de mémoire de la mémoire de la bibliothèque **XLOPER**/ \*\*\*\* temporaire, en libérant toute mémoire déjà allouée.</span><span class="sxs-lookup"><span data-stu-id="50d89-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="50d89-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50d89-107">Parameters</span></span>

<span data-ttu-id="50d89-108">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="50d89-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="50d89-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50d89-109">Return value</span></span>

<span data-ttu-id="50d89-110">Cette fonction ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="50d89-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="50d89-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="50d89-111">Example</span></span>

<span data-ttu-id="50d89-112">Cet exemple utilise la fonction **InitFramework** pour libérer toute la mémoire temporaire.</span><span class="sxs-lookup"><span data-stu-id="50d89-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="50d89-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50d89-113">See also</span></span>



[<span data-ttu-id="50d89-114">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="50d89-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

