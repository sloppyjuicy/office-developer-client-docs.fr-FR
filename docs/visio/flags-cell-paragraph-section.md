---
title: Flags, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346220"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="fbb61-103">Flags, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="fbb61-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="fbb61-104">Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="fbb61-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="fbb61-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="fbb61-105">**Value**</span></span>|<span data-ttu-id="fbb61-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="fbb61-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fbb61-107">0</span><span class="sxs-lookup"><span data-stu-id="fbb61-107">0</span></span>  <br/> |<span data-ttu-id="fbb61-108">Orientation du texte de gauche à droite (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="fbb61-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="fbb61-109">0,1</span><span class="sxs-lookup"><span data-stu-id="fbb61-109">1</span></span>  <br/> |<span data-ttu-id="fbb61-110">Orientation du texte de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="fbb61-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbb61-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="fbb61-111">Remarks</span></span>

<span data-ttu-id="fbb61-112">La valeur de cette cellule correspond au paramètre **direction** de l'onglet **paragraphe** de la boîte de dialogue **texte** (sous l'onglet **Accueil** , cliquez sur la flèche **police** ), qui s'affiche uniquement si une langue qui utilise du texte de scripts complexes a été ajouté dans la boîte de dialogue **Préférences de langue de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="fbb61-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="fbb61-113">(Cliquez **sur Démarrer**, **sur tous les programmes**, sur **Microsoft Office**, sur **outils Microsoft Office**, puis sur **Préférences de langue de Microsoft Office**.)</span><span class="sxs-lookup"><span data-stu-id="fbb61-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="fbb61-114">Pour obtenir une référence à la cellule Flags par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="fbb61-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbb61-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="fbb61-115">Cell name:</span></span>  <br/> |<span data-ttu-id="fbb61-116">Para. Flags [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fbb61-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fbb61-117">Pour obtenir une référence à la cellule Flags à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fbb61-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbb61-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fbb61-118">Section index:</span></span>  <br/> |<span data-ttu-id="fbb61-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="fbb61-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="fbb61-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fbb61-120">Row index:</span></span>  <br/> |<span data-ttu-id="fbb61-121">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fbb61-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fbb61-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fbb61-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fbb61-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="fbb61-123">**visFlags**</span></span> <br/> |
   

