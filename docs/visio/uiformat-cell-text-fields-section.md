---
title: UIFormat, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Définit le format d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
ms.openlocfilehash: 16cefc5f45d6b5f0f677e35bd5d0937d48fb2680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426365"
---
# <a name="uiformat-cell-text-fields-section"></a><span data-ttu-id="9a600-103">UIFormat, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="9a600-103">UIFormat Cell (Text Fields Section)</span></span>

<span data-ttu-id="9a600-104">Définit le format d'un champ inséré dans les versions de Visio antérieures à Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="9a600-104">Determines the format of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a600-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a600-105">Remarks</span></span>

<span data-ttu-id="9a600-p101">Cette cellule n'apparaît pas dans la fenêtre Feuille ShapeSheet. Utilisez-la pour gérer les problèmes de compatibilité avec les versions précédentes, tels que l'enregistrement au format Visio version 5.0 d'un dessin réalisé dans Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="9a600-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="9a600-108">Pour obtenir une référence à la cellule UIFormat par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9a600-108">To get a reference to the UIFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a600-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9a600-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9a600-110">Fields.UIFmt[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9a600-110">Fields.UIFmt[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9a600-111">Pour obtenir une référence à la cellule UIFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9a600-111">To get a reference to the UIFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a600-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9a600-112">Section index:</span></span>  <br/> |<span data-ttu-id="9a600-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="9a600-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="9a600-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9a600-114">Row index:</span></span>  <br/> |<span data-ttu-id="9a600-115">**visRowField**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9a600-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9a600-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9a600-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9a600-117">**visFieldUIFormat**</span><span class="sxs-lookup"><span data-stu-id="9a600-117">**visFieldUIFormat**</span></span> <br/> |
   

