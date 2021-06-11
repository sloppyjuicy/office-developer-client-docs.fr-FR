---
title: UICategory, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Définit la catégorie d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434024"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="d4692-103">UICategory, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="d4692-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="d4692-104">Définit la catégorie d'un champ inséré dans les versions de Visio antérieures à Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="d4692-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4692-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4692-105">Remarks</span></span>

<span data-ttu-id="d4692-p101">Cette cellule n'apparaît pas dans la fenêtre Feuille ShapeSheet. Utilisez-la pour gérer les problèmes de compatibilité avec les versions précédentes, tels que l'enregistrement au format Visio 5.0 d'un dessin réalisé dans Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="d4692-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="d4692-108">Pour obtenir une référence à la cellule UICategory par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d4692-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4692-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d4692-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d4692-110">Fields.UICat[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d4692-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d4692-111">Pour obtenir une référence à la cellule UICategory par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d4692-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4692-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d4692-112">Section index:</span></span>  <br/> |<span data-ttu-id="d4692-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="d4692-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="d4692-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d4692-114">Row index:</span></span>  <br/> |<span data-ttu-id="d4692-115">**visRowField**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d4692-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d4692-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d4692-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d4692-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="d4692-117">**visFieldUICategory**</span></span> <br/> |
   

