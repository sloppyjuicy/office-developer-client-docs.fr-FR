---
title: Value, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Contient la fonction d'un champ.
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430944"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="ed08c-103">Value, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="ed08c-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="ed08c-104">Contient la fonction d'un champ.</span><span class="sxs-lookup"><span data-stu-id="ed08c-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed08c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed08c-105">Remarks</span></span>

<span data-ttu-id="ed08c-106">Vous pouvez définir la valeur de cette cellule au moyen de la boîte de dialogue **Champ** (sous l’onglet **Insertion**, dans le groupe **Texte**, cliquez sur **Champ**).</span><span class="sxs-lookup"><span data-stu-id="ed08c-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="ed08c-107">Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ed08c-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed08c-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ed08c-108">Cell name:</span></span>  <br/> |<span data-ttu-id="ed08c-109">Fields.Value[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ed08c-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ed08c-110">Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ed08c-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed08c-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ed08c-111">Section index:</span></span>  <br/> |<span data-ttu-id="ed08c-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="ed08c-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="ed08c-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ed08c-113">Row index:</span></span>  <br/> |<span data-ttu-id="ed08c-114">**visRowField**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ed08c-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="ed08c-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ed08c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ed08c-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="ed08c-116">**visFieldCell**</span></span> <br/> |
   

