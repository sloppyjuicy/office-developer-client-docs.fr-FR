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
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422767"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="8947f-103">Bullet, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="8947f-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="8947f-104">Détermine le style de puce.</span><span class="sxs-lookup"><span data-stu-id="8947f-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="8947f-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8947f-105">**Value**</span></span>|<span data-ttu-id="8947f-106">**Style de puce**</span><span class="sxs-lookup"><span data-stu-id="8947f-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8947f-107">0</span><span class="sxs-lookup"><span data-stu-id="8947f-107">0</span></span>  <br/> |<span data-ttu-id="8947f-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="8947f-108">None</span></span>  <br/> |
|<span data-ttu-id="8947f-109">0,1</span><span class="sxs-lookup"><span data-stu-id="8947f-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="8947f-110">n°2</span><span class="sxs-lookup"><span data-stu-id="8947f-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="8947f-111">3</span><span class="sxs-lookup"><span data-stu-id="8947f-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="8947f-112">4</span><span class="sxs-lookup"><span data-stu-id="8947f-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="8947f-113">disque</span><span class="sxs-lookup"><span data-stu-id="8947f-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="8947f-114">6.x</span><span class="sxs-lookup"><span data-stu-id="8947f-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="8947f-115">7j/7</span><span class="sxs-lookup"><span data-stu-id="8947f-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="8947f-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8947f-116">Section index:</span></span>  <br/> |<span data-ttu-id="8947f-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8947f-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="8947f-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8947f-118">Row index:</span></span>  <br/> |<span data-ttu-id="8947f-119">**visRowParagraph** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="8947f-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="8947f-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8947f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8947f-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="8947f-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8947f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="8947f-122">Remarks</span></span>

<span data-ttu-id="8947f-123">Vous pouvez également définir la valeur de cette cellule en cliquant avec le bouton droit sur une forme, en pointant sur **Format**, en cliquant sur **Texte**, puis en cliquant sur l’onglet **Puces**.</span><span class="sxs-lookup"><span data-stu-id="8947f-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="8947f-124">Pour obtenir une référence à la cellule Bullet par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8947f-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8947f-125">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="8947f-125">Cell name:</span></span>  <br/> |<span data-ttu-id="8947f-126">Para. Bullet [ *i* ] où *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="8947f-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="8947f-127">Pour obtenir une référence à la cellule Bullet par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8947f-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

