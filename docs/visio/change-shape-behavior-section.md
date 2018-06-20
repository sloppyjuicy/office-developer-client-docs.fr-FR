---
title: Section de comportement de forme de modification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Détermine les propriétés qui sont transférées à partir de la forme ancienne de la forme de remplacement pendant une opération de remplacement. Les valeurs des cellules dans la section comportement de forme de modification de la forme de base forme de remplacement sont lus pendant l’opération de remplacement de forme.
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788230"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="d7762-104">Section de comportement de forme de modification</span><span class="sxs-lookup"><span data-stu-id="d7762-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="d7762-105">Détermine les propriétés qui sont transférées à partir de la forme ancienne de la forme de remplacement pendant une opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d7762-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="d7762-106">Les valeurs des cellules dans la section **Modifier le comportement de la forme** de la forme de base forme de remplacement sont lus pendant l’opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="d7762-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d7762-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7762-107">Remarks</span></span>

<span data-ttu-id="d7762-108">En définissant les cellules dans la section **Modifier le comportement de la forme** , vous pouvez vous assurer que certaines propriétés de la forme de remplacement restent inchangées pendant l’opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d7762-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="d7762-109">Propriétés qui ne sont pas protégées sont mis à jour avec les valeurs de forme local de la forme ancienne lors de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d7762-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="d7762-110">Vous pouvez modifier le remplacement des paramètres de comportement d’une forme de base de forme en modifiant le contrôleur de forme (dans la fenêtre **formes** , la forme avec le bouton droit, pointez sur **Modifier la forme**, puis cliquez sur **Modifier la forme de base**) et modification des valeurs de le [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)et [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) des cellules dans la feuille ShapeSheet de la forme de base.</span><span class="sxs-lookup"><span data-stu-id="d7762-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d7762-111">Vous ne pouvez pas modifier les comportements de remplacement de forme des formes qui sont inclus dans les gabarits intégrés dans Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d7762-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="d7762-112">Pour modifier les comportements de remplacement de forme des formes Visio intégrés, créez un nouveau gabarit et ajoutez la forme que vous souhaitez modifier pour le nouveau gabarit.</span><span class="sxs-lookup"><span data-stu-id="d7762-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

