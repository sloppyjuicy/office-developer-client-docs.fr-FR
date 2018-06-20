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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782129"
---
# <a name="fdance"></a><span data-ttu-id="53122-104">fDance</span><span class="sxs-lookup"><span data-stu-id="53122-104">fDance</span></span>

 <span data-ttu-id="53122-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="53122-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="53122-106">Exemple définies par l’utilisateur de commande qui modifie des cellules sélectionnées autour de la feuille de calcul active jusqu'à ce que l’utilisateur appuie sur **ÉCHAP**.</span><span class="sxs-lookup"><span data-stu-id="53122-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="53122-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, générique, par le biais de laquelle cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="53122-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="53122-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53122-108">Parameters</span></span>

<span data-ttu-id="53122-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="53122-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="53122-110">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="53122-110">Property value/Return value</span></span>

<span data-ttu-id="53122-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="53122-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53122-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="53122-112">Remarks</span></span>

<span data-ttu-id="53122-113">Il s’agit d’un exemple d’une longue opération.</span><span class="sxs-lookup"><span data-stu-id="53122-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="53122-114">Il appelle la fonction [xlAbort](xlabort.md) occasionnellement.</span><span class="sxs-lookup"><span data-stu-id="53122-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="53122-115">Cela donne le processeur (aident à multitâche coopératif) et vérifie si l’utilisateur a appuyé sur **ÉCHAP** pour annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="53122-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="53122-116">Dans ce cas, il offre à l’utilisateur d’annuler l’abandon.</span><span class="sxs-lookup"><span data-stu-id="53122-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="53122-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="53122-117">Example</span></span>

<span data-ttu-id="53122-118">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="53122-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53122-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53122-119">See also</span></span>



[<span data-ttu-id="53122-120">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="53122-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

