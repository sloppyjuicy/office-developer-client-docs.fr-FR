---
title: Change Shape Behavior Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Détermine les propriétés qui sont transférées de l'ancienne forme à la forme de remplacement pendant une opération de remplacement. Les valeurs des cellules dans la section modifier le comportement de la forme de la forme de base du remplacement sont lues pendant l'opération de remplacement de la forme.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418665"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="7ae38-104">Change Shape Behavior Section</span><span class="sxs-lookup"><span data-stu-id="7ae38-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="7ae38-105">Détermine les propriétés qui sont transférées de l'ancienne forme à la forme de remplacement pendant une opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7ae38-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="7ae38-106">Les valeurs des cellules dans la section **modifier le comportement** de la forme de la forme de base du remplacement sont lues pendant l'opération de remplacement de la forme.</span><span class="sxs-lookup"><span data-stu-id="7ae38-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7ae38-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="7ae38-107">Remarks</span></span>

<span data-ttu-id="7ae38-108">En définissant les cellules dans la section **modifier le comportement** de la forme, vous pouvez vous assurer que certaines propriétés de la forme de remplacement restent inchangées lors de l'opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7ae38-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="7ae38-109">Les propriétés qui ne sont pas protégées sont mises à jour avec les valeurs de forme locale de l'ancienne forme pendant l'opération.</span><span class="sxs-lookup"><span data-stu-id="7ae38-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="7ae38-110">Vous pouvez modifier les paramètres de remplacement d'une forme de base en modifiant la forme de base (dans la fenêtre **formes** , cliquez avec le bouton droit sur la forme, pointEz sur modifier la forme de **base**, puis cliquez sur modifier la **forme de base**) et modifiez les valeurs de la [ Cellules ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)et [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) dans la feuille ShapeSheet de la forme de base.</span><span class="sxs-lookup"><span data-stu-id="7ae38-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ae38-111">Vous ne pouvez pas modifier les comportements de remplacement de forme des formes incluses dans les gabarits prédéfinis dans Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="7ae38-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="7ae38-112">Pour modifier les comportements de remplacement de forme des formes Visio prédéfinies, créez un nouveau gabarit et ajoutez la forme que vous souhaitez modifier au nouveau gabarit.</span><span class="sxs-lookup"><span data-stu-id="7ae38-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

