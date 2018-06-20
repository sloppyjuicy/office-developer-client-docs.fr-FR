---
title: Fonction THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs, où la couleur (nombre) passée en tant qu’argument a été modifiée par la valeur spécifiée de teinte ou l’ombre stockée dans les paramètres de dégradé du thème actif.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789895"
---
# <a name="themecbv-function"></a><span data-ttu-id="f89d3-103">Fonction THEMECBV</span><span class="sxs-lookup"><span data-stu-id="f89d3-103">THEMECBV Function</span></span>

<span data-ttu-id="f89d3-104">Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs, où la couleur (nombre) passée en tant qu’argument a été modifiée par la valeur spécifiée de teinte ou l’ombre stockée dans les paramètres de dégradé du thème actif.</span><span class="sxs-lookup"><span data-stu-id="f89d3-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="f89d3-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="f89d3-105">Version Information</span></span>

<span data-ttu-id="f89d3-106">Version ajoutée : Visio 2013</span><span class="sxs-lookup"><span data-stu-id="f89d3-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f89d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f89d3-107">Syntax</span></span>

 <span data-ttu-id="f89d3-108">**THEMECBV** ( _couleur_, _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="f89d3-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="f89d3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f89d3-109">Parameters</span></span>

|<span data-ttu-id="f89d3-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="f89d3-110">**Name**</span></span>|<span data-ttu-id="f89d3-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f89d3-111">**Required/Optional**</span></span>|<span data-ttu-id="f89d3-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f89d3-112">**Data Type**</span></span>|<span data-ttu-id="f89d3-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="f89d3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f89d3-114">_color_</span><span class="sxs-lookup"><span data-stu-id="f89d3-114">_color_</span></span> <br/> |<span data-ttu-id="f89d3-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f89d3-115">Required</span></span>  <br/> |<span data-ttu-id="f89d3-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="f89d3-116">**Number**</span></span> <br/> |<span data-ttu-id="f89d3-117">Nombre représentant un index dans la palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f89d3-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="f89d3-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="f89d3-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="f89d3-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f89d3-119">Required</span></span>  <br/> |<span data-ttu-id="f89d3-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="f89d3-120">**Number**</span></span> <br/> |<span data-ttu-id="f89d3-121">Le point de dégradé (teinte ou l’ombre) stockée dans les paramètres de dégradé à appliquer à la couleur du thème actif.</span><span class="sxs-lookup"><span data-stu-id="f89d3-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="f89d3-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f89d3-122">Return value</span></span>

 <span data-ttu-id="f89d3-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="f89d3-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f89d3-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="f89d3-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="f89d3-125">La fonction THEMECBV n’a aucun effet sur la couleur passée en tant qu’argument si la propriété QuickStyle qui est affectée à la forme n’est pas un dégradé.</span><span class="sxs-lookup"><span data-stu-id="f89d3-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="f89d3-126">Les paramètres de dégradé dans un thème sont une série de points de dégradé numérotée qui correspondent à un « ECLAIRCISSANT » (teinte) ou le « assombrissement » (ombre).</span><span class="sxs-lookup"><span data-stu-id="f89d3-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="f89d3-127">Ces nuances et teintes sont appliqués à une couleur de base pour créer un effet de dégradé.</span><span class="sxs-lookup"><span data-stu-id="f89d3-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="f89d3-128">La fonction **THEMECBV** prend une entrée de couleur et renvoie la couleur une fois qu’il a été modifié par la teinte ou l’ombre du point de dégradé spécifié.</span><span class="sxs-lookup"><span data-stu-id="f89d3-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="f89d3-129">Les teintes et les ombres provenant de la définition du thème, si le style rapide actuel contient un remplissage en dégradé.</span><span class="sxs-lookup"><span data-stu-id="f89d3-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="f89d3-130">Si le Style rapide active ne spécifie pas un remplissage en dégradé ou la forme est définie sur aucun thème, cette formule renvoie simplement la couleur qui a été passée dans pour le premier argument.</span><span class="sxs-lookup"><span data-stu-id="f89d3-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f89d3-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="f89d3-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="f89d3-132">Renvoie la couleur créée en appliquant la teinte ou l’ombre de la cinquième de dégradé du dégradé à la couleur spécifiée dans la cellule **FillForegnd** .</span><span class="sxs-lookup"><span data-stu-id="f89d3-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="f89d3-133">Renvoie une ombre ou teinte de rouge créé en appliquant le deuxième point de dégradé à une couleur de base de rouge.</span><span class="sxs-lookup"><span data-stu-id="f89d3-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

