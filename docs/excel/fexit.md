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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782116"
---
# <a name="fexit"></a><span data-ttu-id="c0f17-104">fExit</span><span class="sxs-lookup"><span data-stu-id="c0f17-104">fExit</span></span>

 <span data-ttu-id="c0f17-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0f17-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0f17-106">Exemple définies par l’utilisateur de commande qui décharge GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="c0f17-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="c0f17-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, générique, par le biais de laquelle cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="c0f17-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="c0f17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0f17-108">Parameters</span></span>

<span data-ttu-id="c0f17-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c0f17-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c0f17-110">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c0f17-110">Property value/Return value</span></span>

<span data-ttu-id="c0f17-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="c0f17-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0f17-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0f17-112">Remarks</span></span>

<span data-ttu-id="c0f17-113">Il s’agit d’une routine initiées par l’utilisateur pour quitter GENERIC.xll doivent éviter d’appeler simplement `UNREGISTER("GENERIC.XLL")` dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c0f17-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="c0f17-114">Ce serait force annuler l’inscription de toutes les fonctions dans cette DLL, même s’ils sont enregistrés quelque part ailleurs.</span><span class="sxs-lookup"><span data-stu-id="c0f17-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="c0f17-115">Annuler l’inscription au lieu de cela, les fonctions d’un à la fois.</span><span class="sxs-lookup"><span data-stu-id="c0f17-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="c0f17-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="c0f17-116">Example</span></span>

<span data-ttu-id="c0f17-117">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c0f17-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0f17-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0f17-118">See also</span></span>



[<span data-ttu-id="c0f17-119">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="c0f17-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

