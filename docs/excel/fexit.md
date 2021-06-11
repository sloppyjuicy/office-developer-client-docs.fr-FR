---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fonction fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429914"
---
# <a name="fexit"></a><span data-ttu-id="c4e8c-104">fExit</span><span class="sxs-lookup"><span data-stu-id="c4e8c-104">fExit</span></span>

 <span data-ttu-id="c4e8c-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c4e8c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c4e8c-106">Exemple de commande définie par l’utilisateur qui décharge GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="c4e8c-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="c4e8c-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="c4e8c-108">Parameters</span></span>

<span data-ttu-id="c4e8c-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c4e8c-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="c4e8c-110">Property value/Return value</span></span>

<span data-ttu-id="c4e8c-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4e8c-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="c4e8c-112">Remarks</span></span>

<span data-ttu-id="c4e8c-113">Il s’agit d’une routine initiée par l’utilisateur pour quitter GENERIC.xll Vous devez éviter  `UNREGISTER("GENERIC.XLL")` d’appeler simplement dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="c4e8c-114">Cela désinsèrerait de force toutes les fonctions dans cette DLL, même si elles sont enregistrées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="c4e8c-115">Au lieu de cela, désinsser les fonctions une par une.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="c4e8c-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4e8c-116">Example</span></span>

<span data-ttu-id="c4e8c-117">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c4e8c-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4e8c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4e8c-118">See also</span></span>



[<span data-ttu-id="c4e8c-119">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="c4e8c-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

