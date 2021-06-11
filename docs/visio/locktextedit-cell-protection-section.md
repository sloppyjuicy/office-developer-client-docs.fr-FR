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
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404497"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="bd970-103">LockTextEdit, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="bd970-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="bd970-104">Verrouille le texte d’une forme afin d’empêcher sa modification.</span><span class="sxs-lookup"><span data-stu-id="bd970-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="bd970-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="bd970-105">**Value**</span></span>|<span data-ttu-id="bd970-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd970-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd970-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bd970-107">TRUE</span></span>  <br/> |<span data-ttu-id="bd970-108">Le texte ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="bd970-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="bd970-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd970-109">FALSE</span></span>  <br/> | <span data-ttu-id="bd970-110">Le texte peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="bd970-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd970-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd970-111">Remarks</span></span>

<span data-ttu-id="bd970-112">Vous pouvez mettre le texte en forme en appliquant un style à l’aide de la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**).</span><span class="sxs-lookup"><span data-stu-id="bd970-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="bd970-113">Pour obtenir une référence à la cellule LockTextEdit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bd970-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd970-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bd970-114">Cell name:</span></span>  <br/> | <span data-ttu-id="bd970-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="bd970-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="bd970-116">Pour obtenir une référence à la cellule LockTextEdit à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bd970-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd970-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bd970-117">Section index:</span></span>  <br/> |<span data-ttu-id="bd970-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd970-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd970-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bd970-119">Row index:</span></span>  <br/> |<span data-ttu-id="bd970-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bd970-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="bd970-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bd970-121">Cell index:</span></span>  <br/> |<span data-ttu-id="bd970-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="bd970-122">**visLockTextEdit**</span></span> <br/> |
   

