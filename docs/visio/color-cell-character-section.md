---
title: Color, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Détermine la couleur utilisée pour le texte de la forme.
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788253"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="8abb5-103">Color, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="8abb5-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="8abb5-104">Détermine la couleur utilisée pour le texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="8abb5-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8abb5-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8abb5-105">Remarks</span></span>

<span data-ttu-id="8abb5-106">Pour définir la couleur, tapez un nombre compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="8abb5-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="8abb5-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="8abb5-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="8abb5-108">La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8abb5-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="8abb5-109">Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus.</span><span class="sxs-lookup"><span data-stu-id="8abb5-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="8abb5-110">Vous pouvez définir une transparence pour la couleur du texte dans la cellule Transparency.</span><span class="sxs-lookup"><span data-stu-id="8abb5-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="8abb5-111">Pour obtenir une référence à la cellule Color par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8abb5-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8abb5-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8abb5-112">Cell name:</span></span>  <br/> |<span data-ttu-id="8abb5-113">Char.Color [ *i* ] où *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="8abb5-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="8abb5-114">Pour obtenir une référence à la cellule Color par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8abb5-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8abb5-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8abb5-115">Section index:</span></span>  <br/> |<span data-ttu-id="8abb5-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="8abb5-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="8abb5-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8abb5-117">Row index:</span></span>  <br/> |<span data-ttu-id="8abb5-118">**visRowCharacter** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="8abb5-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="8abb5-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8abb5-119">Cell index:</span></span>  <br/> |<span data-ttu-id="8abb5-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="8abb5-120">**visCharacterColor**</span></span> <br/> |
   

