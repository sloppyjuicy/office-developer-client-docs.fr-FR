---
title: Bullet, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Détermine le style de puce.
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788187"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="e1139-103">Bullet, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="e1139-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="e1139-104">Détermine le style de puce.</span><span class="sxs-lookup"><span data-stu-id="e1139-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="e1139-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e1139-105">**Value**</span></span>|<span data-ttu-id="e1139-106">**Style de puce**</span><span class="sxs-lookup"><span data-stu-id="e1139-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1139-107">0</span><span class="sxs-lookup"><span data-stu-id="e1139-107">0</span></span>  <br/> |<span data-ttu-id="e1139-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="e1139-108">None</span></span>  <br/> |
|<span data-ttu-id="e1139-109">1</span><span class="sxs-lookup"><span data-stu-id="e1139-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="e1139-110">2</span><span class="sxs-lookup"><span data-stu-id="e1139-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="e1139-111">3</span><span class="sxs-lookup"><span data-stu-id="e1139-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="e1139-112">4</span><span class="sxs-lookup"><span data-stu-id="e1139-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="e1139-113">5</span><span class="sxs-lookup"><span data-stu-id="e1139-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="e1139-114">6</span><span class="sxs-lookup"><span data-stu-id="e1139-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="e1139-115">7</span><span class="sxs-lookup"><span data-stu-id="e1139-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="e1139-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e1139-116">Section index:</span></span>  <br/> |<span data-ttu-id="e1139-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="e1139-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="e1139-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e1139-118">Row index:</span></span>  <br/> |<span data-ttu-id="e1139-119">**visRowParagraph** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="e1139-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="e1139-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e1139-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e1139-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="e1139-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1139-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1139-122">Remarks</span></span>

<span data-ttu-id="e1139-123">Vous pouvez également définir la valeur de cette cellule en cliquant sur une forme, en pointant sur **Format**, en cliquant sur **texte**, puis en cliquant sur l’onglet **puces** .</span><span class="sxs-lookup"><span data-stu-id="e1139-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="e1139-124">Pour obtenir une référence à la cellule Bullet par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e1139-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1139-125">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e1139-125">Cell name:</span></span>  <br/> |<span data-ttu-id="e1139-126">Para.Bullet [ *i* ] où *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="e1139-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="e1139-127">Pour obtenir une référence à la cellule Bullet par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e1139-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

