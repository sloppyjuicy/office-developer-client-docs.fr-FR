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
description: Détermine le calendrier utilisé pour les données de forme lorsque le type de données est Date.
ms.openlocfilehash: 502ecd8a028c4c0d9841bbd3e0ed369f73bd6b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788191"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="6d40c-103">Calendar, cellule (section Custom Properties)</span><span class="sxs-lookup"><span data-stu-id="6d40c-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="6d40c-104">Détermine le calendrier utilisé pour les données de forme lorsque le type de données est Date.</span><span class="sxs-lookup"><span data-stu-id="6d40c-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d40c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d40c-105">Remarks</span></span>

<span data-ttu-id="6d40c-106">Les valeurs possibles sont : 0 (Occidental), 1 (Hijri arabe), 2 (Lunaire hébraïque), 3 (Calendrier taïwanais), 4 (Calendrier impérial japonais), 5 (Bouddhiste Thaï), 6 (Danki coréen), 7 (Hindou ère Saka), 8 (Transcription anglaise) et 9 (Transcription française).</span><span class="sxs-lookup"><span data-stu-id="6d40c-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="6d40c-107">Pour obtenir une référence à la cellule Calendar par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="6d40c-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d40c-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6d40c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6d40c-109">Propriétés.  *nom* . Calendrier où de propriétés.  *Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="6d40c-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6d40c-110">Pour obtenir une référence à la cellule Calendar par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6d40c-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d40c-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6d40c-111">Section index:</span></span>  <br/> |<span data-ttu-id="6d40c-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6d40c-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="6d40c-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6d40c-113">Row index:</span></span>  <br/> |<span data-ttu-id="6d40c-114">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6d40c-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6d40c-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6d40c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6d40c-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="6d40c-116">**visCustPropsCalendar**</span></span> <br/> |
   

