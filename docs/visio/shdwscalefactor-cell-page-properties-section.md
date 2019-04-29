---
title: ShdwScaleFactor, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Indique le pourcentage d'agrandissement ou de réduction de la forme d'une ombre.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429004"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="42f37-103">ShdwScaleFactor, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="42f37-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="42f37-104">Indique le pourcentage d'agrandissement ou de réduction de la forme d'une ombre.</span><span class="sxs-lookup"><span data-stu-id="42f37-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="42f37-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="42f37-105">Remarks</span></span>

<span data-ttu-id="42f37-106">Chaque ombre a un axe d'ombre portée, qui est un point sur l'ombre qui correspond à l'axe de la forme.</span><span class="sxs-lookup"><span data-stu-id="42f37-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="42f37-107">Par exemple, si l'axe d'une forme est au centre de cette dernière, l'axe d'ombre portée est le point central de l'ombre.</span><span class="sxs-lookup"><span data-stu-id="42f37-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="42f37-108">Lors de l'application d'une mise à l'échelle à des ombres simples, le facteur d'agrandissement est centré sur l'emplacement du code confidentiel ombré; lors de l'application d'une mise à l'échelle aux ombres obliques, le facteur d'agrandissement est appliqué dans la direction oblique.</span><span class="sxs-lookup"><span data-stu-id="42f37-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="42f37-109">Ce pourcentage est utilisé lorsque le type d'ombre d'une forme est défini sur page default (la cellule ShapeShdwType est égale à \* \* visFSTPageDefault \* \*).</span><span class="sxs-lookup"><span data-stu-id="42f37-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals \*\* visFSTPageDefault \*\* ).</span></span> 
  
<span data-ttu-id="42f37-110">Pour définir ce comportement pour une forme individuelle, utilisez la cellule ShapeShdwScaleFactor dans la section Fill Format.</span><span class="sxs-lookup"><span data-stu-id="42f37-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="42f37-111">Cette valeur correspond à celle de la zone **Facteur d’agrandissement** sous l’onglet **Ombres** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur **Mise en page**).</span><span class="sxs-lookup"><span data-stu-id="42f37-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="42f37-112">Pour obtenir une référence à la cellule ShdwScaleFactor par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="42f37-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42f37-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="42f37-113">Cell name:</span></span>  <br/> | <span data-ttu-id="42f37-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="42f37-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="42f37-115">Pour obtenir une référence à la cellule ShdwScaleFactor par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="42f37-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42f37-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="42f37-116">Section index:</span></span>  <br/> |<span data-ttu-id="42f37-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="42f37-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="42f37-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="42f37-118">Row index:</span></span>  <br/> |<span data-ttu-id="42f37-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="42f37-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="42f37-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="42f37-120">Cell index:</span></span>  <br/> |<span data-ttu-id="42f37-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="42f37-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

