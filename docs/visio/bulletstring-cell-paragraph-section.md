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
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788194"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="212ad-103">BulletString, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="212ad-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="212ad-104">Permet de créer un style de puce personnalisé.</span><span class="sxs-lookup"><span data-stu-id="212ad-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="212ad-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="212ad-105">Remarks</span></span>

<span data-ttu-id="212ad-p101">Entrez le style sous la forme d’une chaîne (entre guillemets). Par exemple, entrez la chaîne « ooo ».</span><span class="sxs-lookup"><span data-stu-id="212ad-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="212ad-108">Vous pouvez également définir la valeur de cette cellule en cliquant sur une forme, en pointant sur **Format**, en cliquant sur **texte**, puis en cliquant sur l’onglet **puces** .</span><span class="sxs-lookup"><span data-stu-id="212ad-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="212ad-109">Pour obtenir une référence à la cellule BulletString par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="212ad-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="212ad-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="212ad-110">Cell name:</span></span>  <br/> |<span data-ttu-id="212ad-111">Para.BulletStr [ *i* ] où *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="212ad-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="212ad-112">Pour obtenir une référence à la cellule BulletString par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="212ad-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="212ad-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="212ad-113">Section index:</span></span>  <br/> |<span data-ttu-id="212ad-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="212ad-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="212ad-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="212ad-115">Row index:</span></span>  <br/> |<span data-ttu-id="212ad-116">**visRowParagraph** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="212ad-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="212ad-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="212ad-117">Cell index:</span></span>  <br/> |<span data-ttu-id="212ad-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="212ad-118">**visBulletString**</span></span> <br/> |
   

