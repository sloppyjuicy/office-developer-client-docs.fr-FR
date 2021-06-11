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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413114"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="52f9a-103">Flags, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="52f9a-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="52f9a-104">Indique si l'orientation du texte est de gauche à droite ou de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="52f9a-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="52f9a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="52f9a-105">**Value**</span></span>|<span data-ttu-id="52f9a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="52f9a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52f9a-107">0</span><span class="sxs-lookup"><span data-stu-id="52f9a-107">0</span></span>  <br/> |<span data-ttu-id="52f9a-108">Orientation du texte de gauche à droite (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="52f9a-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="52f9a-109">1</span><span class="sxs-lookup"><span data-stu-id="52f9a-109">1</span></span>  <br/> |<span data-ttu-id="52f9a-110">Orientation du texte de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="52f9a-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52f9a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="52f9a-111">Remarks</span></span>

<span data-ttu-id="52f9a-112">La valeur de cette cellule correspond au  paramètre **Direction** sous l’onglet  Paragraphe de  la boîte de dialogue Texte (sous l’onglet Accueil, cliquez sur la flèche Police), qui apparaît uniquement si une langue qui utilise du texte de script complexe a été ajoutée dans la boîte de dialogue Préférences de langue **Microsoft Office.** </span><span class="sxs-lookup"><span data-stu-id="52f9a-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="52f9a-113">(Cliquez **sur** Démarrer, sur Tous les **programmes,** sur **Microsoft Office,** sur Microsoft Office **Outils,** puis sur Microsoft Office **langue.)**</span><span class="sxs-lookup"><span data-stu-id="52f9a-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="52f9a-114">Pour obtenir une référence à la cellule Flags par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="52f9a-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52f9a-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="52f9a-115">Cell name:</span></span>  <br/> |<span data-ttu-id="52f9a-116">Para.Flags[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="52f9a-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="52f9a-117">Pour obtenir une référence à la cellule Flags à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="52f9a-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52f9a-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="52f9a-118">Section index:</span></span>  <br/> |<span data-ttu-id="52f9a-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="52f9a-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="52f9a-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="52f9a-120">Row index:</span></span>  <br/> |<span data-ttu-id="52f9a-121">**visRowParagraph**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="52f9a-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="52f9a-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="52f9a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="52f9a-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="52f9a-123">**visFlags**</span></span> <br/> |
   

