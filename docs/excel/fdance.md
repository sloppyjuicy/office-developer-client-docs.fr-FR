---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fonction fdance [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311038"
---
# <a name="fdance"></a><span data-ttu-id="29ce9-104">fDance</span><span class="sxs-lookup"><span data-stu-id="29ce9-104">fDance</span></span>

 <span data-ttu-id="29ce9-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="29ce9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="29ce9-106">Exemple de commande définie par l'utilisateur qui modifie les cellules sélectionnées de la feuille de calcul active jusqu'à ce que l'utilisateur appuie sur **Échap**.</span><span class="sxs-lookup"><span data-stu-id="29ce9-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="29ce9-107">Lorsque GENERIC. xll est chargé, il crée un menu défini par l'utilisateur, générique, par le biais duquel cette commande est accédée.</span><span class="sxs-lookup"><span data-stu-id="29ce9-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="29ce9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29ce9-108">Parameters</span></span>

<span data-ttu-id="29ce9-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="29ce9-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="29ce9-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="29ce9-110">Property value/Return value</span></span>

<span data-ttu-id="29ce9-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="29ce9-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29ce9-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="29ce9-112">Remarks</span></span>

<span data-ttu-id="29ce9-113">Il s'agit d'un exemple de longue opération.</span><span class="sxs-lookup"><span data-stu-id="29ce9-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="29ce9-114">Il appelle de manière occasionnelle la fonction [xlAbort](xlabort.md) .</span><span class="sxs-lookup"><span data-stu-id="29ce9-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="29ce9-115">Cela génère le processeur (aide au multitâche coopératif) et vérifie si l'utilisateur a appuyé sur **Échap** pour annuler l'opération.</span><span class="sxs-lookup"><span data-stu-id="29ce9-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="29ce9-116">Si c'est le cas, il offre à l'utilisateur la possibilité d'annuler l'abandon.</span><span class="sxs-lookup"><span data-stu-id="29ce9-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="29ce9-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="29ce9-117">Example</span></span>

<span data-ttu-id="29ce9-118">Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="29ce9-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="29ce9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29ce9-119">See also</span></span>



[<span data-ttu-id="29ce9-120">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="29ce9-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

