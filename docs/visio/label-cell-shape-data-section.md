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
description: Indique l’intitulé que les utilisateurs voient s’afficher dans la fenêtre  Données de forme. Un intitulé se compose de caractères alphanumériques dont le caractère de soulignement (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358750"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="8bb57-104">Label, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="8bb57-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="8bb57-105">Indique l’intitulé que les utilisateurs voient s’afficher dans la fenêtre  **Données de forme**.</span><span class="sxs-lookup"><span data-stu-id="8bb57-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="8bb57-106">Un intitulé se compose de caractères alphanumériques dont le caractère de soulignement (_).</span><span class="sxs-lookup"><span data-stu-id="8bb57-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8bb57-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bb57-107">Remarks</span></span>

<span data-ttu-id="8bb57-108">Cet intitulé est automatiquement affiché entre guillemets dans la cellule. Ces guillemets n’apparaissent pas dans la fenêtre **Données de forme**.</span><span class="sxs-lookup"><span data-stu-id="8bb57-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="8bb57-109">Si aucun texte d’intitulé n’est trouvé, Visio affiche le nom de la ligne (Prop.Row) dans la fenêtre **Données de forme**.</span><span class="sxs-lookup"><span data-stu-id="8bb57-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="8bb57-110">Pour obtenir une référence à la cellule Label par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8bb57-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb57-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="8bb57-111">Cell name:</span></span>  <br/> |<span data-ttu-id="8bb57-112">Hélice. *Nom* . Étiquette où prop.  *Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="8bb57-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="8bb57-113">Pour obtenir une référence à la cellule Label à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8bb57-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb57-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8bb57-114">Section index:</span></span>  <br/> |<span data-ttu-id="8bb57-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="8bb57-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="8bb57-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8bb57-116">Row index:</span></span>  <br/> |<span data-ttu-id="8bb57-117">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8bb57-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8bb57-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8bb57-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8bb57-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="8bb57-119">**visCustPropsLabel**</span></span> <br/> |
   

