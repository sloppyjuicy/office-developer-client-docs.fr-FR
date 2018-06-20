---
title: Label, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Indique l’intitulé qui s’affiche dans la fenêtre données de forme. Une étiquette est constituée de caractères alphanumériques, y compris le caractère de soulignement (_).
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788880"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="a645c-104">Label, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="a645c-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="a645c-105">Indique l’intitulé qui s’affiche dans la fenêtre **Données de forme** .</span><span class="sxs-lookup"><span data-stu-id="a645c-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="a645c-106">Une étiquette est constituée de caractères alphanumériques, y compris le caractère de soulignement (_).</span><span class="sxs-lookup"><span data-stu-id="a645c-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a645c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a645c-107">Remarks</span></span>

<span data-ttu-id="a645c-108">L’application insère automatiquement la chaîne d’étiquette entre des guillemets dans la cellule, mais les guillemets ne sont pas affichées dans la fenêtre **Données de forme** .</span><span class="sxs-lookup"><span data-stu-id="a645c-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="a645c-109">Si aucun texte de l’étiquette n’est trouvé, Visio affiche le nom de la ligne (Prop.Row) dans la fenêtre **Données de forme** .</span><span class="sxs-lookup"><span data-stu-id="a645c-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="a645c-110">Pour obtenir une référence à la cellule Label par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="a645c-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a645c-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a645c-111">Cell name:</span></span>  <br/> |<span data-ttu-id="a645c-112">Propriétés. *Nom* . Étiquette où de propriétés.  *Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="a645c-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="a645c-113">Pour obtenir une référence à la cellule Label par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a645c-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a645c-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a645c-114">Section index:</span></span>  <br/> |<span data-ttu-id="a645c-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="a645c-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="a645c-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a645c-116">Row index:</span></span>  <br/> |<span data-ttu-id="a645c-117">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a645c-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a645c-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a645c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a645c-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="a645c-119">**visCustPropsLabel**</span></span> <br/> |
   

