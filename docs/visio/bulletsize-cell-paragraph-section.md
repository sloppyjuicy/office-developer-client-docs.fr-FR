---
title: BulletSize, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Indique la taille d'une puce.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405421"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="f4322-103">BulletSize, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="f4322-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="f4322-104">Indique la taille d'une puce.</span><span class="sxs-lookup"><span data-stu-id="f4322-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4322-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4322-105">Remarks</span></span>

<span data-ttu-id="f4322-106">Cette valeur peut être spécifiée pour des puces prédéfinies ou personnalisées, sous forme de pourcentage ou de valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f4322-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="f4322-107">Si la valeur est égale à zéro (0), la puce est de la même taille de police que le premier caractère du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="f4322-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="f4322-108">Si la valeur est un pourcentage, la puce a pour taille un pourcentage de la taille de police du premier caractère du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="f4322-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="f4322-109">Les nombres négatifs sont traités comme des pourcentages.</span><span class="sxs-lookup"><span data-stu-id="f4322-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="f4322-110">Pour obtenir une référence à la cellule BulletSize par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f4322-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4322-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f4322-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f4322-112">Para. BulletFontSize [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f4322-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f4322-113">Pour obtenir une référence à la cellule BulletSize à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f4322-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4322-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f4322-114">Section index:</span></span>  <br/> |<span data-ttu-id="f4322-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="f4322-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="f4322-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f4322-116">Row index:</span></span>  <br/> |<span data-ttu-id="f4322-117">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f4322-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f4322-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f4322-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f4322-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="f4322-119">**visBulletFontSize**</span></span> <br/> |
   

