---
title: PreviewQuality, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789330"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="ed765-103">PreviewQuality, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="ed765-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="ed765-104">Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.</span><span class="sxs-lookup"><span data-stu-id="ed765-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="ed765-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ed765-105">**Value**</span></span>|<span data-ttu-id="ed765-106">**Qualité d’aperçu**</span><span class="sxs-lookup"><span data-stu-id="ed765-106">**Preview quality**</span></span>|<span data-ttu-id="ed765-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="ed765-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ed765-108">0</span><span class="sxs-lookup"><span data-stu-id="ed765-108">0</span></span>  <br/> | <span data-ttu-id="ed765-109">Brouillon</span><span class="sxs-lookup"><span data-stu-id="ed765-109">Draft</span></span>  <br/> |<span data-ttu-id="ed765-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="ed765-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="ed765-111">1</span><span class="sxs-lookup"><span data-stu-id="ed765-111">1</span></span>  <br/> | <span data-ttu-id="ed765-112">Détaillé</span><span class="sxs-lookup"><span data-stu-id="ed765-112">Detailed</span></span>  <br/> |<span data-ttu-id="ed765-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="ed765-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed765-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed765-114">Remarks</span></span>

<span data-ttu-id="ed765-115">Vous pouvez également définir cette valeur sur l’onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur le bouton **Office** , cliquez sur l’onglet **Infos** , cliquez sur **Propriétés du Document**, puis cliquez sur **Propriétés avancées**).</span><span class="sxs-lookup"><span data-stu-id="ed765-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="ed765-116">Pour obtenir une référence à la cellule PreviewQuality par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="ed765-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed765-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ed765-117">Cell name:</span></span>  <br/> | <span data-ttu-id="ed765-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="ed765-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="ed765-119">Pour obtenir une référence à la cellule PreviewQuality par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ed765-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed765-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ed765-120">Section index:</span></span>  <br/> |<span data-ttu-id="ed765-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ed765-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ed765-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ed765-122">Row index:</span></span>  <br/> |<span data-ttu-id="ed765-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="ed765-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="ed765-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ed765-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ed765-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="ed765-125">**visDocPreviewQuality**</span></span> <br/> |
   

