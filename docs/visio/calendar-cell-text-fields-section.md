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
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424751"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="aef23-103">Calendar, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="aef23-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="aef23-104">Détermine le calendrier utilisé pour un champ de texte lorsque le type de données est Date.</span><span class="sxs-lookup"><span data-stu-id="aef23-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aef23-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="aef23-105">Remarks</span></span>

<span data-ttu-id="aef23-106">Les valeurs possibles sont : 0 (Occidental), 1 (Hijri arabe), 2 (Lunaire hébraïque), 3 (Calendrier taïwanais), 4 (Calendrier impérial japonais), 5 (Bouddhiste Thaï), 6 (Danki coréen), 7 (Hindou ère Saka), 8 (Transcription anglaise) et 9 (Transcription française).</span><span class="sxs-lookup"><span data-stu-id="aef23-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="aef23-107">Pour obtenir une référence à la cellule Calendar par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="aef23-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aef23-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="aef23-108">Cell name:</span></span>  <br/> | <span data-ttu-id="aef23-109">Fields.Calendar[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="aef23-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="aef23-110">Pour obtenir une référence à la cellule Calendar à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="aef23-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aef23-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="aef23-111">Section index:</span></span>  <br/> |<span data-ttu-id="aef23-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="aef23-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="aef23-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="aef23-113">Row index:</span></span>  <br/> |<span data-ttu-id="aef23-114">**visRowField**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="aef23-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="aef23-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="aef23-115">Cell index:</span></span>  <br/> |<span data-ttu-id="aef23-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="aef23-116">**visFieldCalendar**</span></span> <br/> |
   

