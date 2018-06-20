---
title: TxtPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Détermine la valeur y-coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789953"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="17a53-104">TxtPinY, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="17a53-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="17a53-105">Détermine la valeur *y* -coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="17a53-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="17a53-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="17a53-106">The default formula is:</span></span> 
  
<span data-ttu-id="17a53-107">= Hauteur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="17a53-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17a53-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="17a53-108">Remarks</span></span>

<span data-ttu-id="17a53-109">Pour obtenir une référence à la cellule TxtPinY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="17a53-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17a53-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="17a53-110">Cell name:</span></span>  <br/> | <span data-ttu-id="17a53-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="17a53-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="17a53-112">Pour obtenir une référence à la cellule TxtPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="17a53-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17a53-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="17a53-113">Section index:</span></span>  <br/> |<span data-ttu-id="17a53-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17a53-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17a53-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="17a53-115">Row index:</span></span>  <br/> |<span data-ttu-id="17a53-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="17a53-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="17a53-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="17a53-117">Cell index:</span></span>  <br/> |<span data-ttu-id="17a53-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="17a53-118">**visXFormPinY**</span></span> <br/> |
   

