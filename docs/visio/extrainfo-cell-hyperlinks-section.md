---
title: ExtraInfo, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Représente une chaîne qui passe l'information à utiliser dans la résolution d'une URL, comme les coordonnées d'un point dans une image interactive. Par exemple, dans la cellule ExtraInfo, x =&amp;41 y = 7specifies les coordonnées d'une image interactive.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409572"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="a7964-104">ExtraInfo, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="a7964-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="a7964-105">Représente une chaîne qui passe l'information à utiliser dans la résolution d'une URL, comme les coordonnées d'un point dans une image interactive.</span><span class="sxs-lookup"><span data-stu-id="a7964-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="a7964-106">Par exemple, dans la cellule ExtraInfo, «x =&amp;41 y = 7» spécifie les coordonnées d'une image interactive.</span><span class="sxs-lookup"><span data-stu-id="a7964-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7964-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7964-107">Remarks</span></span>

<span data-ttu-id="a7964-108">Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.</span><span class="sxs-lookup"><span data-stu-id="a7964-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="a7964-109">Pour obtenir une référence à la cellule ExtraInfo par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a7964-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a7964-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a7964-110">Cell name:</span></span>  <br/> | <span data-ttu-id="a7964-111">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="a7964-111">Hyperlink.</span></span>  <span data-ttu-id="a7964-112">*nom* . ExtraInfo, où hyperLink.</span><span class="sxs-lookup"><span data-stu-id="a7964-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="a7964-113">*Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="a7964-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="a7964-114">Pour obtenir une référence à la cellule ExtraInfo à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a7964-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a7964-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a7964-115">Section index:</span></span>  <br/> |<span data-ttu-id="a7964-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="a7964-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="a7964-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a7964-117">Row index:</span></span>  <br/> |<span data-ttu-id="a7964-118">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a7964-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a7964-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a7964-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a7964-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="a7964-120">**visHLinkExtraInfo**</span></span> <br/> |
   

