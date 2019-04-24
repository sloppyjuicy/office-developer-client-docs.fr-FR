---
title: Name, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Contient le nom du réviseur d’un document.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335167"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="3a203-103">Name, cellule (section Reviewer)</span><span class="sxs-lookup"><span data-stu-id="3a203-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="3a203-104">Contient le nom du réviseur d’un document.</span><span class="sxs-lookup"><span data-stu-id="3a203-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a203-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a203-105">Remarks</span></span>

 <span data-ttu-id="3a203-106">Cette valeur est définie par défaut sur le nom figurant dans la zone **nom d'utilisateur** de l'onglet **général** de la boîte de dialogue **options Visio** (cliquez sur l'onglet **fichier** , sur **options**, puis sur **général**).</span><span class="sxs-lookup"><span data-stu-id="3a203-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="3a203-107">Pour obtenir une référence à la cellule Name par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="3a203-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a203-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="3a203-108">Cell name:</span></span>  <br/> | <span data-ttu-id="3a203-109">Reviewer.Name [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3a203-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3a203-110">Pour obtenir une référence à la cellule Name à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a203-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a203-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3a203-111">Section index:</span></span>  <br/> |<span data-ttu-id="3a203-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="3a203-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="3a203-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3a203-113">Row index:</span></span>  <br/> |<span data-ttu-id="3a203-114">**visRowReviewer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3a203-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3a203-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3a203-115">Cell index:</span></span>  <br/> |<span data-ttu-id="3a203-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="3a203-116">**visReviewerName**</span></span> <br/> |
   

