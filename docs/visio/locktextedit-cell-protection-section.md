---
title: LockTextEdit, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Verrouille le texte d’une forme afin d’empêcher sa modification.
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789022"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="4c2d4-103">LockTextEdit, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="4c2d4-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="4c2d4-104">Verrouille le texte d’une forme afin d’empêcher sa modification.</span><span class="sxs-lookup"><span data-stu-id="4c2d4-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="4c2d4-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4c2d4-105">**Value**</span></span>|<span data-ttu-id="4c2d4-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c2d4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c2d4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4c2d4-107">TRUE</span></span>  <br/> |<span data-ttu-id="4c2d4-108">Le texte ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="4c2d4-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="4c2d4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4c2d4-109">FALSE</span></span>  <br/> | <span data-ttu-id="4c2d4-110">Le texte peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="4c2d4-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c2d4-111">Note</span><span class="sxs-lookup"><span data-stu-id="4c2d4-111">Remarks</span></span>

<span data-ttu-id="4c2d4-112">Vous pouvez mettre le texte en forme en appliquant un style dans la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ).</span><span class="sxs-lookup"><span data-stu-id="4c2d4-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="4c2d4-113">Pour obtenir une référence à la cellule LockTextEdit par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="4c2d4-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c2d4-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4c2d4-114">Cell name:</span></span>  <br/> | <span data-ttu-id="4c2d4-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="4c2d4-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="4c2d4-116">Pour obtenir une référence à la cellule LockTextEdit par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4c2d4-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c2d4-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4c2d4-117">Section index:</span></span>  <br/> |<span data-ttu-id="4c2d4-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4c2d4-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4c2d4-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4c2d4-119">Row index:</span></span>  <br/> |<span data-ttu-id="4c2d4-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="4c2d4-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="4c2d4-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4c2d4-121">Cell index:</span></span>  <br/> |<span data-ttu-id="4c2d4-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="4c2d4-122">**visLockTextEdit**</span></span> <br/> |
   

