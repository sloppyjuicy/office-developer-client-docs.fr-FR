---
title: DoubleStrikethrough, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Détermine si du texte est barré double.
ms.openlocfilehash: dcd7c7769da8298c1f6ab474d2b63fc982f479b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788524"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="df7f2-103">DoubleStrikethrough, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="df7f2-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="df7f2-104">Détermine si du texte est barré double.</span><span class="sxs-lookup"><span data-stu-id="df7f2-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df7f2-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="df7f2-105">Remarks</span></span>

<span data-ttu-id="df7f2-106">Pour obtenir une référence à la cellule DoubleStrikethrough par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="df7f2-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df7f2-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="df7f2-107">Cell name:</span></span>  <br/> | <span data-ttu-id="df7f2-108">Char.DoubleStrikethrough [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="df7f2-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="df7f2-109">Pour obtenir une référence à la cellule DoubleStrikethrough par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="df7f2-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df7f2-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="df7f2-110">Section index:</span></span>  <br/> |<span data-ttu-id="df7f2-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="df7f2-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="df7f2-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="df7f2-112">Row index:</span></span>  <br/> |<span data-ttu-id="df7f2-113">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="df7f2-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="df7f2-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="df7f2-114">Cell index:</span></span>  <br/> |<span data-ttu-id="df7f2-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="df7f2-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

