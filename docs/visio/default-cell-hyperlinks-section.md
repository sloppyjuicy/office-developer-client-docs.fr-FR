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
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434353"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="24085-104">Default, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="24085-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="24085-p102">Détermine le lien hypertexte par défaut d'une forme ou d'une page. Définissez la valeur de cette cellule comme TRUE pour définir un lien hypertexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="24085-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24085-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="24085-107">Remarks</span></span>

<span data-ttu-id="24085-p103">Vous pouvez également définir le lien hypertexte par défaut en sélectionnant une forme et en cliquant sur **Lien hypertexte** sous l’onglet **Insertion**, en sélectionnant ensuite un lien hypertexte, puis en cliquant sur **Par défaut**. Le lien hypertexte par défaut s’affiche en texte gras.</span><span class="sxs-lookup"><span data-stu-id="24085-p103">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**. The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="24085-110">Pour obtenir une référence à la cellule Default par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="24085-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24085-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="24085-111">Cell name:</span></span>  <br/> |<span data-ttu-id="24085-112">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="24085-112">Hyperlink.</span></span> <span data-ttu-id="24085-113">*Nom*  . Par défaut où Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="24085-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="24085-114">*Le nom*  est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="24085-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="24085-115">Pour obtenir une référence à la cellule Default à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="24085-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24085-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="24085-116">Section index:</span></span>  <br/> |<span data-ttu-id="24085-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="24085-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="24085-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="24085-118">Row index:</span></span>  <br/> |<span data-ttu-id="24085-119">**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="24085-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="24085-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="24085-120">Cell index:</span></span>  <br/> |<span data-ttu-id="24085-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="24085-121">**visHLinkDefault**</span></span> <br/> |
   

