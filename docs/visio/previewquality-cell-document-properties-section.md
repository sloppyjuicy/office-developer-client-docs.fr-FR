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
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416817"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="cac24-103">PreviewQuality, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="cac24-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="cac24-104">Détermine si l'aperçu du dessin est en mode brouillon ou détaillé.</span><span class="sxs-lookup"><span data-stu-id="cac24-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="cac24-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="cac24-105">**Value**</span></span>|<span data-ttu-id="cac24-106">**Qualité d'aperçu**</span><span class="sxs-lookup"><span data-stu-id="cac24-106">**Preview quality**</span></span>|<span data-ttu-id="cac24-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="cac24-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="cac24-108">0</span><span class="sxs-lookup"><span data-stu-id="cac24-108">0</span></span>  <br/> | <span data-ttu-id="cac24-109">Brouillon</span><span class="sxs-lookup"><span data-stu-id="cac24-109">Draft</span></span>  <br/> |<span data-ttu-id="cac24-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="cac24-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="cac24-111">1 </span><span class="sxs-lookup"><span data-stu-id="cac24-111">1</span></span>  <br/> | <span data-ttu-id="cac24-112">Détails</span><span class="sxs-lookup"><span data-stu-id="cac24-112">Detailed</span></span>  <br/> |<span data-ttu-id="cac24-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="cac24-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cac24-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cac24-114">Remarks</span></span>

<span data-ttu-id="cac24-115">Vous pouvez également définir  cette valeur sous  l’onglet Résumé dans la  boîte de dialogue Propriétés (cliquez sur le bouton **Office,** sur l’onglet Informations, sur Propriétés du **document,** puis sur Propriétés **avancées).**</span><span class="sxs-lookup"><span data-stu-id="cac24-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="cac24-116">Pour obtenir une référence à la cellule PreviewQuality par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="cac24-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cac24-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="cac24-117">Cell name:</span></span>  <br/> | <span data-ttu-id="cac24-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="cac24-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="cac24-119">Pour obtenir une référence à la cellule PreviewQuality à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="cac24-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cac24-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="cac24-120">Section index:</span></span>  <br/> |<span data-ttu-id="cac24-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cac24-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cac24-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="cac24-122">Row index:</span></span>  <br/> |<span data-ttu-id="cac24-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="cac24-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="cac24-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="cac24-124">Cell index:</span></span>  <br/> |<span data-ttu-id="cac24-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="cac24-125">**visDocPreviewQuality**</span></span> <br/> |
   

