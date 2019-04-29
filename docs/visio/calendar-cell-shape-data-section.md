---
title: Calendar, cellule (section Custom Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Détermine le calendrier utilisé pour les données de forme lorsque le type de données est date.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432757"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="f8099-103">Calendar, cellule (section Custom Properties)</span><span class="sxs-lookup"><span data-stu-id="f8099-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="f8099-104">Détermine le calendrier utilisé pour les données de forme lorsque le type de données est date.</span><span class="sxs-lookup"><span data-stu-id="f8099-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8099-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8099-105">Remarks</span></span>

<span data-ttu-id="f8099-106">Les valeurs possibles sont : 0 (Occidental), 1 (Hijri arabe), 2 (Lunaire hébraïque), 3 (Calendrier taïwanais), 4 (Calendrier impérial japonais), 5 (Bouddhiste Thaï), 6 (Danki coréen), 7 (Hindou ère Saka), 8 (Transcription anglaise) et 9 (Transcription française).</span><span class="sxs-lookup"><span data-stu-id="f8099-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="f8099-107">Pour obtenir une référence à la cellule Calendar par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f8099-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8099-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f8099-108">Cell name:</span></span>  <br/> | <span data-ttu-id="f8099-109">Hélice.  *nom* . Calendrier où prop.  *Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="f8099-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f8099-110">Pour obtenir une référence à la cellule Calendar à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f8099-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8099-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f8099-111">Section index:</span></span>  <br/> |<span data-ttu-id="f8099-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="f8099-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="f8099-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f8099-113">Row index:</span></span>  <br/> |<span data-ttu-id="f8099-114">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f8099-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f8099-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f8099-115">Cell index:</span></span>  <br/> |<span data-ttu-id="f8099-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="f8099-116">**visCustPropsCalendar**</span></span> <br/> |
   

