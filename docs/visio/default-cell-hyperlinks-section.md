---
title: Default, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Détermine le lien hypertexte par défaut d'une forme ou d'une page. Définissez la valeur de cette cellule comme TRUE pour définir un lien hypertexte par défaut.
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788439"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="6d386-104">Default, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="6d386-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="6d386-p102">Détermine le lien hypertexte par défaut d'une forme ou d'une page. Définissez la valeur de cette cellule comme TRUE pour définir un lien hypertexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="6d386-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d386-107">Note</span><span class="sxs-lookup"><span data-stu-id="6d386-107">Remarks</span></span>

<span data-ttu-id="6d386-108">Vous pouvez également définir le lien hypertexte par défaut en sélectionnant une forme, en cliquant sur le **lien hypertexte** sous l’onglet **Insertion** , sélectionnez un lien hypertexte, puis en cliquant sur **par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6d386-108">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**.</span></span> <span data-ttu-id="6d386-109">Le lien hypertexte par défaut s’affiche en gras.</span><span class="sxs-lookup"><span data-stu-id="6d386-109">The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="6d386-110">Pour obtenir une référence à la cellule Default par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="6d386-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d386-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6d386-111">Cell name:</span></span>  <br/> |<span data-ttu-id="6d386-112">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="6d386-112">Hyperlink.</span></span> <span data-ttu-id="6d386-113">*Nom* . Par défaut où un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="6d386-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="6d386-114">*Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="6d386-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6d386-115">Pour obtenir une référence à la cellule Default par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6d386-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d386-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6d386-116">Section index:</span></span>  <br/> |<span data-ttu-id="6d386-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="6d386-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="6d386-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6d386-118">Row index:</span></span>  <br/> |<span data-ttu-id="6d386-119">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6d386-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6d386-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6d386-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6d386-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="6d386-121">**visHLinkDefault**</span></span> <br/> |
   

