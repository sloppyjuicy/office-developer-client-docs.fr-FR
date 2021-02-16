---
title: BulletString, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Permet de créer un style de puce personnalisé.
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409747"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="c4f9d-103">BulletString, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="c4f9d-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="c4f9d-104">Permet de créer un style de puce personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c4f9d-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c4f9d-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c4f9d-105">Remarks</span></span>

<span data-ttu-id="c4f9d-p101">Entrez le style sous la forme d’une chaîne (entre guillemets). Par exemple, entrez la chaîne « ooo ».</span><span class="sxs-lookup"><span data-stu-id="c4f9d-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="c4f9d-108">Vous pouvez également définir la valeur de cette cellule en cliquant avec le bouton droit sur une forme, en pointant sur **Format**, en cliquant sur **Texte**, puis en cliquant sur l’onglet **Puces**.</span><span class="sxs-lookup"><span data-stu-id="c4f9d-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="c4f9d-109">Pour obtenir une référence à la cellule BulletString par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="c4f9d-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4f9d-110">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="c4f9d-110">Cell name:</span></span>  <br/> |<span data-ttu-id="c4f9d-111">Para.BulletStr[ *i*  ] où  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="c4f9d-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="c4f9d-112">Pour obtenir une référence à la cellule BulletString à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c4f9d-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4f9d-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c4f9d-113">Section index:</span></span>  <br/> |<span data-ttu-id="c4f9d-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c4f9d-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="c4f9d-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c4f9d-115">Row index:</span></span>  <br/> |<span data-ttu-id="c4f9d-116">**visRowParagraph**  +   *i* où *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="c4f9d-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="c4f9d-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c4f9d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c4f9d-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="c4f9d-118">**visBulletString**</span></span> <br/> |
   

