---
title: Frame, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432855"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="75f1c-104">Frame, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="75f1c-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="75f1c-p102">Représente le nom d'un cadre à prendre comme destination lorsque l'application est ouverte comme document actif dans une application conteneur. La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="75f1c-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75f1c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="75f1c-107">Remarks</span></span>

<span data-ttu-id="75f1c-108">Pour obtenir une référence à la cellule Frame par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="75f1c-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75f1c-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="75f1c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="75f1c-110">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="75f1c-110">Hyperlink.</span></span>  <span data-ttu-id="75f1c-111">*nom*  . Cadre où lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="75f1c-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="75f1c-112">*nom est*  le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="75f1c-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="75f1c-113">Pour obtenir une référence à la cellule Frame à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="75f1c-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75f1c-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="75f1c-114">Section index:</span></span>  <br/> |<span data-ttu-id="75f1c-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="75f1c-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="75f1c-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="75f1c-116">Row index:</span></span>  <br/> |<span data-ttu-id="75f1c-117">**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="75f1c-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="75f1c-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="75f1c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="75f1c-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="75f1c-119">**visHLinkFrame**</span></span> <br/> |
   

