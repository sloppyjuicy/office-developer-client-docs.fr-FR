---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fonction fexit [Excel 2007]
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
# <a name="fexit"></a><span data-ttu-id="997d8-104">fExit</span><span class="sxs-lookup"><span data-stu-id="997d8-104">fExit</span></span>

 <span data-ttu-id="997d8-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="997d8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="997d8-106">Exemple de commande définie par l'utilisateur qui décharge GENERIC. XLL.</span><span class="sxs-lookup"><span data-stu-id="997d8-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="997d8-107">Lorsque GENERIC. xll est chargé, il crée un menu défini par l'utilisateur, générique, par le biais duquel cette commande est accédée.</span><span class="sxs-lookup"><span data-stu-id="997d8-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="997d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="997d8-108">Parameters</span></span>

<span data-ttu-id="997d8-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="997d8-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="997d8-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="997d8-110">Property value/Return value</span></span>

<span data-ttu-id="997d8-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="997d8-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="997d8-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="997d8-112">Remarks</span></span>

<span data-ttu-id="997d8-113">Il s'agit d'une routine initiée par l'utilisateur pour quitter GENERIC. xll vous `UNREGISTER("GENERIC.XLL")` devez éviter d'appeler simplement dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="997d8-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="997d8-114">Cela forcerait l'annulation de l'inscription de toutes les fonctions de cette DLL, même si elles sont enregistrées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="997d8-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="997d8-115">Au lieu de cela, annulez l'inscription des fonctions une par une.</span><span class="sxs-lookup"><span data-stu-id="997d8-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="997d8-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="997d8-116">Example</span></span>

<span data-ttu-id="997d8-117">Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="997d8-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="997d8-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="997d8-118">See also</span></span>



[<span data-ttu-id="997d8-119">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="997d8-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

