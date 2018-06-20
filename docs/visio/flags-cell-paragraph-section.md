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
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788633"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="733fb-103">Flags, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="733fb-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="733fb-104">Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="733fb-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="733fb-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="733fb-105">**Value**</span></span>|<span data-ttu-id="733fb-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="733fb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="733fb-107">0</span><span class="sxs-lookup"><span data-stu-id="733fb-107">0</span></span>  <br/> |<span data-ttu-id="733fb-108">Orientation du texte de gauche à droite (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="733fb-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="733fb-109">1</span><span class="sxs-lookup"><span data-stu-id="733fb-109">1</span></span>  <br/> |<span data-ttu-id="733fb-110">Orientation du texte de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="733fb-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="733fb-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="733fb-111">Remarks</span></span>

<span data-ttu-id="733fb-112">La valeur de cette cellule correspond au paramètre **orientation** de l’onglet **paragraphe** dans la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ), qui s’affiche uniquement si le texte de scripts une langue qui utilise un type complexe a été ajouté dans la boîte de dialogue **Préférences linguistiques de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="733fb-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="733fb-113">(Cliquez sur **Démarrer**, sur **Tous les programmes**, sur **Microsoft Office**, sur **Outils Microsoft Office**, puis cliquez sur **Préférences linguistiques de Microsoft Office**.)</span><span class="sxs-lookup"><span data-stu-id="733fb-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="733fb-114">Pour obtenir une référence à la cellule Flags par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="733fb-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="733fb-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="733fb-115">Cell name:</span></span>  <br/> |<span data-ttu-id="733fb-116">Para.Flags [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="733fb-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="733fb-117">Pour obtenir une référence à la cellule Flags par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="733fb-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="733fb-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="733fb-118">Section index:</span></span>  <br/> |<span data-ttu-id="733fb-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="733fb-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="733fb-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="733fb-120">Row index:</span></span>  <br/> |<span data-ttu-id="733fb-121">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="733fb-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="733fb-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="733fb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="733fb-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="733fb-123">**visFlags**</span></span> <br/> |
   

