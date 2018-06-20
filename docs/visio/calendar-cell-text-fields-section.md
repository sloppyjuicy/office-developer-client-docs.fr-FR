---
title: Calendar, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date.
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788171"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="81362-103">Calendar, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="81362-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="81362-104">Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date.</span><span class="sxs-lookup"><span data-stu-id="81362-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81362-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="81362-105">Remarks</span></span>

<span data-ttu-id="81362-106">Les valeurs possibles sont : 0 (Occidental), 1 (Hijri arabe), 2 (Lunaire hébraïque), 3 (Calendrier taïwanais), 4 (Calendrier impérial japonais), 5 (Bouddhiste Thaï), 6 (Danki coréen), 7 (Hindou ère Saka), 8 (Transcription anglaise) et 9 (Transcription française).</span><span class="sxs-lookup"><span data-stu-id="81362-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="81362-107">Pour obtenir une référence à la cellule Calendar par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="81362-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81362-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="81362-108">Cell name:</span></span>  <br/> | <span data-ttu-id="81362-109">Fields.Calendar [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="81362-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="81362-110">Pour obtenir une référence à la cellule Calendar par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="81362-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81362-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="81362-111">Section index:</span></span>  <br/> |<span data-ttu-id="81362-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="81362-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="81362-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="81362-113">Row index:</span></span>  <br/> |<span data-ttu-id="81362-114">**visRowField** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="81362-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="81362-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="81362-115">Cell index:</span></span>  <br/> |<span data-ttu-id="81362-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="81362-116">**visFieldCalendar**</span></span> <br/> |
   

