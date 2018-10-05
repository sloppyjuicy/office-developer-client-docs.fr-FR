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
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385479"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="4e8ef-103">Cellule ButtonFace (section Balises d’action)</span><span class="sxs-lookup"><span data-stu-id="4e8ef-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="4e8ef-104">Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4e8ef-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="4e8ef-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4e8ef-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4e8ef-106">Remarks</span></span>

<span data-ttu-id="4e8ef-p101">La chaîne contenue dans la cellule ButtonFace représente l’ID d’une image de face de bouton Microsoft Office. Une valeur de 0 (zéro) ou vide applique par défaut le bouton d’information « i » standard des balises d’action</span><span class="sxs-lookup"><span data-stu-id="4e8ef-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Bouton d’informations sur la balise « i » action standard](media/InfoPS_ZA10180114.gif)<span data-ttu-id="4e8ef-110">.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-110"></span></span>
  
<span data-ttu-id="4e8ef-111">Les ID qui peuvent être utilisées dans la cellule ButtonFace sont les mêmes que ceux utilisés avec la propriété **FaceID** d’un objet **CommandBarButton** .</span><span class="sxs-lookup"><span data-stu-id="4e8ef-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="4e8ef-112">Pour plus d’informations sur ces codes, recherchez « utilisation des images de boutons de barre de commande » sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="4e8ef-113">Pour obtenir une référence à la cellule ButtonFace par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="4e8ef-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e8ef-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4e8ef-114">Cell name:</span></span>  <br/> | <span data-ttu-id="4e8ef-115">Balises actives.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-115">SmartTags.</span></span>  <span data-ttu-id="4e8ef-116">*nom* . ButtonFace où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="4e8ef-117">*nom* est le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="4e8ef-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="4e8ef-118">Pour obtenir une référence à la cellule ButtonFace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4e8ef-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e8ef-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4e8ef-119">Section index:</span></span>  <br/> |<span data-ttu-id="4e8ef-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="4e8ef-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="4e8ef-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4e8ef-121">Row index:</span></span>  <br/> |<span data-ttu-id="4e8ef-122">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4e8ef-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4e8ef-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4e8ef-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4e8ef-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="4e8ef-124">**visSmartTagButtonFace**</span></span> <br/> |
   

