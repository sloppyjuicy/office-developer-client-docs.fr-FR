---
title: Calendar, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Détermine le calendrier utilisé lorsqu'une formule de cellule contient des informations de Date.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421815"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="c0aa1-103">Calendar, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="c0aa1-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c0aa1-104">Détermine le calendrier utilisé lorsqu'une formule de cellule contient des informations de Date.</span><span class="sxs-lookup"><span data-stu-id="c0aa1-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0aa1-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0aa1-105">Remarks</span></span>

<span data-ttu-id="c0aa1-106">Les valeurs possibles sont : 0 (Occidental), 1 (Hijri arabe), 2 (Lunaire hébraïque), 3 (Calendrier taïwanais), 4 (Calendrier impérial japonais), 5 (Bouddhiste Thaï), 6 (Danki coréen), 7 (Hindou ère Saka), 8 (Transcription anglaise) et 9 (Transcription française).</span><span class="sxs-lookup"><span data-stu-id="c0aa1-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="c0aa1-107">Pour obtenir une référence à la cellule Calendar par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="c0aa1-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0aa1-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c0aa1-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c0aa1-109">Calendrier</span><span class="sxs-lookup"><span data-stu-id="c0aa1-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="c0aa1-110">Pour obtenir une référence à la cellule Calendar à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c0aa1-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0aa1-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c0aa1-111">Section index:</span></span>  <br/> |<span data-ttu-id="c0aa1-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0aa1-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0aa1-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c0aa1-113">Row index:</span></span>  <br/> |<span data-ttu-id="c0aa1-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c0aa1-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c0aa1-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c0aa1-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c0aa1-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="c0aa1-116">**visObjCalendar**</span></span> <br/> |
   

