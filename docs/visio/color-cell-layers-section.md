---
title: Color, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Indique la couleur utilisée pour afficher le calque.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341824"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="a40a4-103">Color, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="a40a4-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="a40a4-104">Indique la couleur utilisée pour afficher le calque.</span><span class="sxs-lookup"><span data-stu-id="a40a4-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a40a4-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="a40a4-105">Remarks</span></span>

<span data-ttu-id="a40a4-106">Pour définir la couleur, tapez un nombre compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="a40a4-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="a40a4-107">Cette valeur de cellule correspond au **paramètre couleur de calque** dans la boîte de dialogue Propriétés des **calques** (dans le groupe **modification** de l'onglet **Accueil** , cliquez sur **calques** , puis sur Propriétés des **calques**).</span><span class="sxs-lookup"><span data-stu-id="a40a4-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="a40a4-108">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="a40a4-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="a40a4-109">La valeur d'une couleur personnalisée est sa couleur RVB et la valeur RVB ( *r, v, b*), au lieu d'un nombre, est affichée dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a40a4-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="a40a4-110">Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24.</span><span class="sxs-lookup"><span data-stu-id="a40a4-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="a40a4-111">Une valeur de 255 indique que le calque n'a pas de couleur.</span><span class="sxs-lookup"><span data-stu-id="a40a4-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="a40a4-112">Vous pouvez définir la transparence de la couleur du calque dans la cellule Transparency.</span><span class="sxs-lookup"><span data-stu-id="a40a4-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="a40a4-113">Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a40a4-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a40a4-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a40a4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="a40a4-115">Layers. Color [ *i* ] où *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="a40a4-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="a40a4-116">Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a40a4-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a40a4-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a40a4-117">Section index:</span></span>  <br/> |<span data-ttu-id="a40a4-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="a40a4-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="a40a4-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a40a4-119">Row index:</span></span>  <br/> |<span data-ttu-id="a40a4-120">**visRowLayer** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="a40a4-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="a40a4-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a40a4-121">Cell index:</span></span>  <br/> |<span data-ttu-id="a40a4-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="a40a4-122">**visLayerColor**</span></span> <br/> |
   

