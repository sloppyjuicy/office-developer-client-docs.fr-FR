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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396623"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="b8b25-103">Cellule Description (section Liens hypertexte)</span><span class="sxs-lookup"><span data-stu-id="b8b25-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="b8b25-104">Représente une chaîne de texte descriptive d’un lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="b8b25-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b8b25-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8b25-105">Remarks</span></span>

<span data-ttu-id="b8b25-106">Utilisez cette cellule pour stocker des commentaires sur le lien hypertexte. par exemple, « un lien vers notre site prix. »</span><span class="sxs-lookup"><span data-stu-id="b8b25-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="b8b25-107">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Liens hypertexte** (cliquez sur **Liens hypertexte** sous l’onglet **Insertion**).</span><span class="sxs-lookup"><span data-stu-id="b8b25-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="b8b25-108">Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b8b25-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8b25-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b8b25-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b8b25-110">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="b8b25-110">Hyperlink.</span></span>  <span data-ttu-id="b8b25-111">*Nom* . Description où un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="b8b25-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="b8b25-112">*Nom* est le nom de la ligne hyperlink</span><span class="sxs-lookup"><span data-stu-id="b8b25-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="b8b25-113">Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b8b25-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8b25-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b8b25-114">Section index:</span></span>  <br/> |<span data-ttu-id="b8b25-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="b8b25-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="b8b25-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b8b25-116">Row index:</span></span>  <br/> |<span data-ttu-id="b8b25-117">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b8b25-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b8b25-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b8b25-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b8b25-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="b8b25-119">**visHLinkDescription**</span></span> <br/> |
   

