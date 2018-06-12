---
title: ButtonFace, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788183"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="0a1e3-103">ButtonFace, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="0a1e3-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="0a1e3-104">Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0a1e3-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="0a1e3-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0a1e3-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0a1e3-106">Remarks</span></span>

<span data-ttu-id="0a1e3-p101">La chaîne contenue dans la cellule ButtonFace représente l'ID d'une image de bouton Microsoft Office. Une valeur de zéro (0) ou vide indique qu'aucune icône ne s'affiche.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="0a1e3-109">Les ID qui peuvent être utilisées dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d’un objet **CommandBarButton** .</span><span class="sxs-lookup"><span data-stu-id="0a1e3-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="0a1e3-110">Pour plus d’informations sur ces codes, recherchez « utilisation des images de boutons de barre de commande » sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="0a1e3-111">Pour obtenir une référence à la cellule ButtonFace par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="0a1e3-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a1e3-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0a1e3-112">Cell name:</span></span>  <br/> |<span data-ttu-id="0a1e3-113">**Actions**.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-113">**Actions**.</span></span>  <span data-ttu-id="0a1e3-114">*nom* .</span><span class="sxs-lookup"><span data-stu-id="0a1e3-114">*name*  .</span></span> <span data-ttu-id="0a1e3-115">**ButtonFace** où **Actions**.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="0a1e3-116">*nom* est le nom de la ligne actions</span><span class="sxs-lookup"><span data-stu-id="0a1e3-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="0a1e3-117">Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0a1e3-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a1e3-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0a1e3-118">Section index:</span></span>  <br/> |<span data-ttu-id="0a1e3-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="0a1e3-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="0a1e3-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0a1e3-120">Row index:</span></span>  <br/> |<span data-ttu-id="0a1e3-121">**visRowAction** +  *i* où **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0a1e3-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0a1e3-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0a1e3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0a1e3-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="0a1e3-123">**visActionButtonFace**</span></span> <br/> |
   

