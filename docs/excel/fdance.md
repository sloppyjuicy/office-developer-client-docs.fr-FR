---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fonction fdance [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409047"
---
# <a name="fdance"></a><span data-ttu-id="89ba9-104">fDance</span><span class="sxs-lookup"><span data-stu-id="89ba9-104">fDance</span></span>

 <span data-ttu-id="89ba9-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="89ba9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="89ba9-106">Exemple de commande définie par l’utilisateur qui modifie les cellules sélectionnées dans la feuille de calcul active jusqu’à ce que l’utilisateur appuie sur **ÉCHAP**.</span><span class="sxs-lookup"><span data-stu-id="89ba9-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="89ba9-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="89ba9-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="89ba9-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="89ba9-108">Parameters</span></span>

<span data-ttu-id="89ba9-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="89ba9-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="89ba9-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="89ba9-110">Property value/Return value</span></span>

<span data-ttu-id="89ba9-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="89ba9-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89ba9-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="89ba9-112">Remarks</span></span>

<span data-ttu-id="89ba9-113">Il s’agit d’un exemple d’une opération longue.</span><span class="sxs-lookup"><span data-stu-id="89ba9-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="89ba9-114">Il appelle parfois la fonction [xlAbort.](xlabort.md)</span><span class="sxs-lookup"><span data-stu-id="89ba9-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="89ba9-115">Cela permet au processeur (d’aider à la multitâche multinationale) et de vérifier si l’utilisateur a appuyer sur **ÉCHAP** pour annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="89ba9-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="89ba9-116">Si c’est le cas, il offre à l’utilisateur la possibilité d’annuler l’abandon.</span><span class="sxs-lookup"><span data-stu-id="89ba9-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="89ba9-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="89ba9-117">Example</span></span>

<span data-ttu-id="89ba9-118">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="89ba9-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89ba9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89ba9-119">See also</span></span>



[<span data-ttu-id="89ba9-120">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="89ba9-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

