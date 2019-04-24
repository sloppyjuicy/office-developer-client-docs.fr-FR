---
title: Description, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Représente une chaîne de texte descriptive d’un lien hypertexte
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360241"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="f638e-103">Description, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="f638e-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="f638e-104">Représente une chaîne de texte descriptive d’un lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="f638e-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f638e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f638e-105">Remarks</span></span>

<span data-ttu-id="f638e-106">Utilisez cette cellule pour stocker des commentaires sur le lien hypertexte; par exemple, «lien vers le site Web de nos tarifs».</span><span class="sxs-lookup"><span data-stu-id="f638e-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="f638e-107">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Liens hypertexte** (cliquez sur **Liens hypertexte** sous l’onglet **Insertion**).</span><span class="sxs-lookup"><span data-stu-id="f638e-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="f638e-108">Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f638e-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f638e-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="f638e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f638e-110">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="f638e-110">Hyperlink.</span></span>  <span data-ttu-id="f638e-111">*Nom* . Description, où hyperLink.</span><span class="sxs-lookup"><span data-stu-id="f638e-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="f638e-112">*Name* est le nom de la ligne de lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="f638e-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="f638e-113">Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f638e-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f638e-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f638e-114">Section index:</span></span>  <br/> |<span data-ttu-id="f638e-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="f638e-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="f638e-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f638e-116">Row index:</span></span>  <br/> |<span data-ttu-id="f638e-117">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f638e-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f638e-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f638e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f638e-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="f638e-119">**visHLinkDescription**</span></span> <br/> |
   

