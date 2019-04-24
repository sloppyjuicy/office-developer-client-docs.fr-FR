---
title: UICode, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Définit le code d'un champ inséré dans les versions de Visio antérieures à Visio 2000.
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327342"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="d2fa6-103">UICode, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="d2fa6-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="d2fa6-104">Définit le code d'un champ inséré dans les versions de Visio antérieures à Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="d2fa6-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2fa6-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2fa6-105">Remarks</span></span>

<span data-ttu-id="d2fa6-p101">Cette cellule n'apparaît pas dans la fenêtre Feuille ShapeSheet. Utilisez-la pour gérer les problèmes de compatibilité avec les versions précédentes, tels que l'enregistrement au format Visio version 5.0 d'un dessin réalisé dans Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="d2fa6-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="d2fa6-108">Pour obtenir une référence à la cellule UICode par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d2fa6-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2fa6-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2fa6-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d2fa6-110">Fields. UICod [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d2fa6-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d2fa6-111">Pour obtenir une référence à la cellule UICode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d2fa6-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2fa6-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d2fa6-112">Section index:</span></span>  <br/> |<span data-ttu-id="d2fa6-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="d2fa6-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="d2fa6-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d2fa6-114">Row index:</span></span>  <br/> |<span data-ttu-id="d2fa6-115">**visRowField** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d2fa6-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d2fa6-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2fa6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d2fa6-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="d2fa6-117">**visFieldUICode**</span></span> <br/> |
   

