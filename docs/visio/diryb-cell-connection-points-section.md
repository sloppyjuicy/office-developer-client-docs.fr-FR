---
title: DirY / B, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Détermine le composant y pour le vecteur d’alignement requis d’un point de connexion correspondant. Cette cellule sert également à orienter la branche reliée d'un lien dynamique. Elle accepte une valeur à virgule flottante.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417090"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="10bcc-105">DirY / B, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="10bcc-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="10bcc-106">Détermine le  *composant y*  pour le vecteur d’alignement requis d’un point de connexion correspondant.</span><span class="sxs-lookup"><span data-stu-id="10bcc-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="10bcc-107">Cette cellule sert également à orienter la branche reliée d'un lien dynamique.</span><span class="sxs-lookup"><span data-stu-id="10bcc-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="10bcc-108">Cette cellule prend pour valeur un réel à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="10bcc-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10bcc-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="10bcc-109">Remarks</span></span>

<span data-ttu-id="10bcc-110">Pour obtenir une référence à la cellule DirY / B par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="10bcc-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10bcc-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10bcc-111">Cell name:</span></span>  <br/> |<span data-ttu-id="10bcc-112">Connections.DirY[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="10bcc-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="10bcc-113">Pour obtenir une référence à la cellule DirY / B à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="10bcc-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10bcc-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="10bcc-114">Section index:</span></span>  <br/> |<span data-ttu-id="10bcc-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="10bcc-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="10bcc-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="10bcc-116">Row index:</span></span>  <br/> |<span data-ttu-id="10bcc-117">**visRowConnectionPts**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="10bcc-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="10bcc-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10bcc-118">Cell index:</span></span>  <br/> |<span data-ttu-id="10bcc-119">**visCnnctDirY** (lignes non étendues)           **visCnnctB** (lignes étendues)</span><span class="sxs-lookup"><span data-stu-id="10bcc-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="10bcc-120">Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.</span><span class="sxs-lookup"><span data-stu-id="10bcc-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

