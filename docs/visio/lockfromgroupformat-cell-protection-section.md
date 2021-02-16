---
title: LockFromGroupFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426057"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="46356-102">LockFromGroupFormat, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="46356-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="46356-103">Bloque la propagation des modifications de format d’une forme de groupe à ses sous-formes, tout en permettant aux utilisateurs de mettre en forme les sous-formes sélectionnées directement.</span><span class="sxs-lookup"><span data-stu-id="46356-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="46356-104">La valeur de la cellule LockFromGroupFormat correspond au paramétrage de la case à cocher **Contre la mise en forme de groupe** de la boîte de dialogue **Protection**.</span><span class="sxs-lookup"><span data-stu-id="46356-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="46356-105">Pour faire référence à la cellule LockFromGroupFormat par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :

</span><span class="sxs-lookup"><span data-stu-id="46356-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46356-106">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="46356-106">Cell name:</span></span>  <br/> |<span data-ttu-id="46356-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="46356-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="46356-108">Pour faire référence à la cellule LockFromGroupFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="46356-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46356-109">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="46356-109">Section index:</span></span>  <br/> |<span data-ttu-id="46356-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="46356-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="46356-111">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="46356-111">Row index:</span></span>  <br/> |<span data-ttu-id="46356-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="46356-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="46356-113">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="46356-113">Cell index:</span></span>  <br/> |<span data-ttu-id="46356-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="46356-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="46356-115">La valeur par défaut de la cellule est 0 (False).</span><span class="sxs-lookup"><span data-stu-id="46356-115">The default value for the cell is 0 (False).</span></span>
  

