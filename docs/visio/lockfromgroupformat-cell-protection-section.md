---
title: LockFromGroupFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789014"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="86e17-102">LockFromGroupFormat, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="86e17-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="86e17-103">Blocs de format des modifications à une forme de groupe soient propagées à ses sous-formes, tout en permettant aux utilisateurs de mettre en forme directement les sous-formes sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="86e17-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="86e17-104">La valeur de la cellule LockFromGroupFormat correspond au paramètre **de groupe mise en forme de** case à cocher dans la boîte de dialogue **Protection** .</span><span class="sxs-lookup"><span data-stu-id="86e17-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="86e17-105">Pour faire référence à la cellule LockFromGroupFormat par un nom à partir d’une autre formule ou d’un programme, utilisez la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="86e17-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86e17-106">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="86e17-106">Cell name:</span></span>  <br/> |<span data-ttu-id="86e17-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="86e17-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="86e17-108">Pour faire référence à la cellule LockFromGroupFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="86e17-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86e17-109">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="86e17-109">Section index:</span></span>  <br/> |<span data-ttu-id="86e17-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="86e17-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="86e17-111">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="86e17-111">Row index:</span></span>  <br/> |<span data-ttu-id="86e17-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="86e17-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="86e17-113">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="86e17-113">Cell index:</span></span>  <br/> |<span data-ttu-id="86e17-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="86e17-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="86e17-115">La valeur par défaut de la cellule est 0 (False).</span><span class="sxs-lookup"><span data-stu-id="86e17-115">The default value for the cell is 0 (False).</span></span>
  

