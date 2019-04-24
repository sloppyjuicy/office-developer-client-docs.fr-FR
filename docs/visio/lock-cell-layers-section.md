---
title: Lock, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification.
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359681"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="b44fc-103">Lock, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="b44fc-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="b44fc-104">Indique si les formes appartenant au calque sont verrouillées en sélection ou en modification.</span><span class="sxs-lookup"><span data-stu-id="b44fc-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="b44fc-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b44fc-105">**Value**</span></span>|<span data-ttu-id="b44fc-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b44fc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b44fc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b44fc-107">TRUE</span></span>  <br/> |<span data-ttu-id="b44fc-108">Les formes sont verrouillées.</span><span class="sxs-lookup"><span data-stu-id="b44fc-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="b44fc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b44fc-109">FALSE</span></span>  <br/> |<span data-ttu-id="b44fc-110">Aucune forme n'est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="b44fc-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b44fc-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b44fc-111">Remarks</span></span>

<span data-ttu-id="b44fc-112">Vous pouvez également définir cette valeur en activant la case à cocher **Verrouiller** dans la boîte de dialogue **Propriétés des calques**(sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis cliquez sur **Propriétés des calques**).</span><span class="sxs-lookup"><span data-stu-id="b44fc-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="b44fc-113">Pour obtenir une référence à la cellule Lock par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b44fc-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b44fc-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b44fc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="b44fc-115">Layers. Locked [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b44fc-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b44fc-116">Pour obtenir une référence à la cellule Lock à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b44fc-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b44fc-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b44fc-117">Section index:</span></span>  <br/> |<span data-ttu-id="b44fc-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="b44fc-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="b44fc-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b44fc-119">Row index:</span></span>  <br/> |<span data-ttu-id="b44fc-120">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b44fc-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b44fc-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b44fc-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b44fc-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="b44fc-122">**visLayerLock**</span></span> <br/> |
   

