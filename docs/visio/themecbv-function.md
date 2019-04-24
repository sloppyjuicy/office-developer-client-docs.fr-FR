---
title: Fonction THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs du document, où la couleur (numérique) transmise en tant qu'argument a été modifiée par la valeur de teinte ou d'ombrage stockée dans les paramètres de dégradé du thème actif.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332262"
---
# <a name="themecbv-function"></a><span data-ttu-id="3fa01-103">Fonction THEMECBV</span><span class="sxs-lookup"><span data-stu-id="3fa01-103">THEMECBV Function</span></span>

<span data-ttu-id="3fa01-104">Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs du document, où la couleur (numérique) transmise en tant qu'argument a été modifiée par la valeur de teinte ou d'ombrage stockée dans les paramètres de dégradé du thème actif.</span><span class="sxs-lookup"><span data-stu-id="3fa01-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="3fa01-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="3fa01-105">Version Information</span></span>

<span data-ttu-id="3fa01-106">Version ajoutée : Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="3fa01-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3fa01-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fa01-107">Syntax</span></span>

 <span data-ttu-id="3fa01-108">**THEMECBV** ( _couleur_, _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="3fa01-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="3fa01-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fa01-109">Parameters</span></span>

|<span data-ttu-id="3fa01-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3fa01-110">**Name**</span></span>|<span data-ttu-id="3fa01-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3fa01-111">**Required/Optional**</span></span>|<span data-ttu-id="3fa01-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3fa01-112">**Data Type**</span></span>|<span data-ttu-id="3fa01-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="3fa01-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3fa01-114">_color_</span><span class="sxs-lookup"><span data-stu-id="3fa01-114">_color_</span></span> <br/> |<span data-ttu-id="3fa01-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3fa01-115">Required</span></span>  <br/> |<span data-ttu-id="3fa01-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="3fa01-116">**Number**</span></span> <br/> |<span data-ttu-id="3fa01-117">Un nombre représentant un index dans la palette de couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="3fa01-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="3fa01-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="3fa01-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="3fa01-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3fa01-119">Required</span></span>  <br/> |<span data-ttu-id="3fa01-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="3fa01-120">**Number**</span></span> <br/> |<span data-ttu-id="3fa01-121">Point de dégradé (teinte ou ombre) stocké dans les paramètres de dégradé du thème actif à appliquer à la couleur.</span><span class="sxs-lookup"><span data-stu-id="3fa01-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="3fa01-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3fa01-122">Return value</span></span>

 <span data-ttu-id="3fa01-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="3fa01-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3fa01-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fa01-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="3fa01-125">La fonction THEMECBV n'a aucun effet sur la couleur transmise en tant qu'argument si le QuickStyle affecté à la forme n'a pas de dégradé.</span><span class="sxs-lookup"><span data-stu-id="3fa01-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="3fa01-126">Les paramètres de dégradé d'un thème sont une série de points de dégradé numérotés correspondant à une «éclaircie» (teinte) ou à un «assombrissement» (ombre).</span><span class="sxs-lookup"><span data-stu-id="3fa01-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="3fa01-127">Ces nuances et teintes sont appliquées à une couleur de base pour créer un effet de couleur de dégradé.</span><span class="sxs-lookup"><span data-stu-id="3fa01-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="3fa01-128">La fonction **THEMECBV** prend une entrée de couleur et renvoie la couleur après qu'elle a été modifiée par la teinte ou l'ombrage du point de dégradé spécifié.</span><span class="sxs-lookup"><span data-stu-id="3fa01-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="3fa01-129">Si le style rapide actif contient un remplissage en dégradé, les teintes et les ombres proviennent de la définition du thème.</span><span class="sxs-lookup"><span data-stu-id="3fa01-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="3fa01-130">Si le style rapide actif ne spécifie pas de remplissage en dégradé ou si la forme n'est pas définie sur aucun thème, cette formule renvoie simplement la couleur qui a été transmise pour le premier argument.</span><span class="sxs-lookup"><span data-stu-id="3fa01-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3fa01-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="3fa01-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="3fa01-132">Renvoie la couleur créée en appliquant la teinte ou l'ombre du cinquième point de dégradé du dégradé à la couleur spécifiée dans la cellule **FillForegnd** .</span><span class="sxs-lookup"><span data-stu-id="3fa01-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="3fa01-133">Renvoie une ombre ou teinte de rouge créée en appliquant le second point de dégradé à une couleur de base de rouge.</span><span class="sxs-lookup"><span data-stu-id="3fa01-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

