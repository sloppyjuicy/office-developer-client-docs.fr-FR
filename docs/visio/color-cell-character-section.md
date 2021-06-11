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
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439988"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="ef6e6-103">Color, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="ef6e6-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="ef6e6-104">Détermine la couleur utilisée pour le texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="ef6e6-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef6e6-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ef6e6-105">Remarks</span></span>

<span data-ttu-id="ef6e6-106">Pour définir la couleur, tapez un nombre compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="ef6e6-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="ef6e6-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="ef6e6-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="ef6e6-108">La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), plutôt qu’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ef6e6-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="ef6e6-109">Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24.</span><span class="sxs-lookup"><span data-stu-id="ef6e6-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="ef6e6-110">Vous pouvez définir une transparence pour la couleur du texte dans la cellule Transparency.</span><span class="sxs-lookup"><span data-stu-id="ef6e6-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="ef6e6-111">Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ef6e6-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef6e6-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ef6e6-112">Cell name:</span></span>  <br/> |<span data-ttu-id="ef6e6-113">Char.Color[ *i*  ] où  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="ef6e6-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="ef6e6-114">Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ef6e6-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef6e6-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ef6e6-115">Section index:</span></span>  <br/> |<span data-ttu-id="ef6e6-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="ef6e6-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="ef6e6-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ef6e6-117">Row index:</span></span>  <br/> |<span data-ttu-id="ef6e6-118">**visRowCharacter**  +   *i* où *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="ef6e6-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="ef6e6-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ef6e6-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ef6e6-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="ef6e6-120">**visCharacterColor**</span></span> <br/> |
   

