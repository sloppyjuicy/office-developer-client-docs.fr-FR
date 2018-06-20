---
title: USE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Applique le motif de trait, motif de remplissage ou extrémité de trait appelé nom à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789978"
---
# <a name="use-function"></a><span data-ttu-id="d0177-103">USE, fonction</span><span class="sxs-lookup"><span data-stu-id="d0177-103">USE Function</span></span>

<span data-ttu-id="d0177-104">Applique le motif de trait, motif de remplissage ou extrémité de trait appelé _nom_ à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.</span><span class="sxs-lookup"><span data-stu-id="d0177-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d0177-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0177-105">Syntax</span></span>

<span data-ttu-id="d0177-106">UTILISATION (« ** *nom* ** »)</span><span class="sxs-lookup"><span data-stu-id="d0177-106">USE(" ** *name* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d0177-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0177-107">Parameters</span></span>

|<span data-ttu-id="d0177-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d0177-108">**Name**</span></span>|<span data-ttu-id="d0177-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d0177-109">**Required/Optional**</span></span>|<span data-ttu-id="d0177-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d0177-110">**Data Type**</span></span>|<span data-ttu-id="d0177-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0177-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d0177-112">_nom_</span><span class="sxs-lookup"><span data-stu-id="d0177-112">_name_</span></span> <br/> |<span data-ttu-id="d0177-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d0177-113">Required</span></span>  <br/> |<span data-ttu-id="d0177-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0177-114">**String**</span></span> <br/> |<span data-ttu-id="d0177-115">Chaîne correspondant à un nom de forme de base valide.</span><span class="sxs-lookup"><span data-stu-id="d0177-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d0177-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d0177-116">Return value</span></span>

<span data-ttu-id="d0177-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0177-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0177-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0177-118">Remarks</span></span>

<span data-ttu-id="d0177-119">Si une forme de base appelée _nom_ est présent dans le gabarit de document du document, le motif est appliqué comme un motif de trait, motif de remplissage, flèche de départ ou flèche de fin.</span><span class="sxs-lookup"><span data-stu-id="d0177-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="d0177-120">Cette fonction renvoie toujours 254.</span><span class="sxs-lookup"><span data-stu-id="d0177-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="d0177-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="d0177-121">Example</span></span>

<span data-ttu-id="d0177-122">USE("Voies ferrées")</span><span class="sxs-lookup"><span data-stu-id="d0177-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="d0177-123">Formate la forme en appliquant le motif de base intitulé Voies ferrées à la forme contenant la formule.</span><span class="sxs-lookup"><span data-stu-id="d0177-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

