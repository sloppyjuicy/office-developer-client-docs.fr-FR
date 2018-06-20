---
title: ButtonFace, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action.
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788184"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="3012b-103">ButtonFace, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="3012b-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="3012b-104">Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="3012b-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3012b-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="3012b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3012b-106">Notes</span><span class="sxs-lookup"><span data-stu-id="3012b-106">Remarks</span></span>

<span data-ttu-id="3012b-107">La chaîne contenue dans la cellule ButtonFace représente l’ID d’une image de bouton Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="3012b-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="3012b-108">La valeur 0 (zéro) ou vide par défaut, le bouton informations de la balise « i » action standard ![](media/InfoPS_ZA10180114.gif).</span><span class="sxs-lookup"><span data-stu-id="3012b-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button ![](media/InfoPS_ZA10180114.gif).</span></span>
  
<span data-ttu-id="3012b-109">Les ID qui peuvent être utilisées dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d’un objet **CommandBarButton** .</span><span class="sxs-lookup"><span data-stu-id="3012b-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="3012b-110">Pour plus d’informations sur ces codes, recherchez « utilisation des images de boutons de barre de commande » sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="3012b-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="3012b-111">Pour obtenir une référence à la cellule ButtonFace par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="3012b-111">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3012b-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3012b-112">Cell name:</span></span>  <br/> | <span data-ttu-id="3012b-113">Balises actives.</span><span class="sxs-lookup"><span data-stu-id="3012b-113">SmartTags.</span></span>  <span data-ttu-id="3012b-114">*nom* . ButtonFace où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3012b-114">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="3012b-115">*nom* est le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="3012b-115">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3012b-116">Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3012b-116">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3012b-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3012b-117">Section index:</span></span>  <br/> |<span data-ttu-id="3012b-118">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3012b-118">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3012b-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3012b-119">Row index:</span></span>  <br/> |<span data-ttu-id="3012b-120">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3012b-120">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3012b-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3012b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="3012b-122">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="3012b-122">**visSmartTagButtonFace**</span></span> <br/> |
   

