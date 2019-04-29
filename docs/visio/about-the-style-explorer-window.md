---
title: À propos de la fenêtre Explorateur de styles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: La fenêtre Explorateur de styles fournit aux développeurs de formes un moyen rapide de déterminer quelles cellules de forme héritent d’un style donné ou quel style transmet sa valeur à une cellule donnée.
ms.openlocfilehash: 55800b692443bae3720b433e5a6178f2709d3675
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431784"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="ca004-103">À propos de la fenêtre Explorateur de styles</span><span class="sxs-lookup"><span data-stu-id="ca004-103">About the Style Explorer Window</span></span>

<span data-ttu-id="ca004-104">La fenêtre **Explorateur de styles** fournit aux développeurs de formes un moyen rapide de déterminer quelles cellules de forme héritent d’un style donné ou quel style transmet sa valeur à une cellule donnée.</span><span class="sxs-lookup"><span data-stu-id="ca004-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="ca004-p101">Les styles sont des collections nommées d’attributs de mise en forme applicables à une forme. Dans Microsoft Visio, un style unique peut définir du texte, une ligne et des attributs de remplissage constituant ainsi un moyen efficace d’assurer la cohérence de vos formes. En outre, vous pouvez également définir un style pour n’importe quelle classe d’attributs (texte, trait ou remplissage) ou n’importe quelle combinaison d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ca004-p101">Styles are named collections of formatting attributes that you can apply to a shape. In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes. Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="ca004-108">À la différence des formes auxquelles vous avez affecté des attributs de mise en forme individuellement, les formes qui tirent leur mise en forme d’un style sont non seulement cohérentes, mais répondent également mieux lors de leur création, déplacement, mise à l’échelle ou rotation.</span><span class="sxs-lookup"><span data-stu-id="ca004-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="ca004-109">La fenêtre **Explorateur de styles** fournit les informations dont vous avez besoin pour mieux comprendre les implications des modifications apportées aux formes.</span><span class="sxs-lookup"><span data-stu-id="ca004-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ca004-110">Les valeurs de cellule qui s’affichent en noir dans la fenêtre ShapeSheet sont héritées ; celles qui s’affichent en bleu sont locales.</span><span class="sxs-lookup"><span data-stu-id="ca004-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="ca004-111">Utilisation de la Fenêtre Explorateur de styles</span><span class="sxs-lookup"><span data-stu-id="ca004-111">Using the Style Explorer window</span></span>

<span data-ttu-id="ca004-112">Pour afficher la **fenêtre Explorateur de styles** , lorsque la fenêtre ShapeSheet est active, sous l'onglet Outils de **feuille ShapeSheet** , dans le groupe **affichage** , sélectionnez **Explorateur de styles**.</span><span class="sxs-lookup"><span data-stu-id="ca004-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="ca004-113">La fenêtre **Explorateur de styles** apparaît ancrée dans la fenêtre ShapeSheet par défaut, mais est une fenêtre ancrée qui peut être ancrée, flottante ou fusionnée avec d'autres fenêtres ShapeSheet ancrées disponibles, par exemple, la fenêtre suivi des **formules** .</span><span class="sxs-lookup"><span data-stu-id="ca004-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="ca004-114">La fenêtre **Explorateur de styles** contient un affichage TreeView de tous les styles définis dans le dessin actif.</span><span class="sxs-lookup"><span data-stu-id="ca004-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ca004-115">Pour plus d’informations sur un style, vous pouvez cliquer avec le bouton droit de la souris dans la fenêtre **Explorateur de styles** pour afficher sa feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ca004-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="ca004-116">La fenêtre **Explorateur de styles** fournit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ca004-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="ca004-117">Cellules qui héritent leurs valeurs d’un style défini.Lorsque vous sélectionnez un style dans la fenêtre **Explorateur de styles**, toutes les cellules de la fenêtre ShapeSheet qui héritent de ce style apparaissent sans hachure, alors que les cellules qui n’héritent pas de ce style apparaissent légèrement hachurées.</span><span class="sxs-lookup"><span data-stu-id="ca004-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="ca004-118">Style transmettant sa valeur à une cellule sélectionnée.Lorsque vous sélectionnez une cellule ShapeSheet, le style transmettant sa valeur s’affiche dans la barre des tâches sous la fenêtre ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ca004-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

