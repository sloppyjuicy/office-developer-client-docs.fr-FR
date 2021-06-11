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
description: Applique le nom appelé motif de trait, motif de remplissage ou fin de trait à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422823"
---
# <a name="use-function"></a><span data-ttu-id="1ddc9-103">Fonction USE</span><span class="sxs-lookup"><span data-stu-id="1ddc9-103">USE Function</span></span>

<span data-ttu-id="1ddc9-104">Applique le nom appelé motif de  trait, motif de remplissage ou fin de trait à la forme lorsqu’il est placé dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1ddc9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ddc9-105">Syntax</span></span>

<span data-ttu-id="1ddc9-106">USE( » \*\* *name* \*\* « )</span><span class="sxs-lookup"><span data-stu-id="1ddc9-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1ddc9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ddc9-107">Parameters</span></span>

|<span data-ttu-id="1ddc9-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1ddc9-108">**Name**</span></span>|<span data-ttu-id="1ddc9-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="1ddc9-109">**Required/Optional**</span></span>|<span data-ttu-id="1ddc9-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="1ddc9-110">**Data Type**</span></span>|<span data-ttu-id="1ddc9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="1ddc9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1ddc9-112">_nom_</span><span class="sxs-lookup"><span data-stu-id="1ddc9-112">_name_</span></span> <br/> |<span data-ttu-id="1ddc9-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1ddc9-113">Required</span></span>  <br/> |<span data-ttu-id="1ddc9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1ddc9-114">**String**</span></span> <br/> |<span data-ttu-id="1ddc9-115">Chaîne correspondant à un nom de forme de base valide.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1ddc9-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1ddc9-116">Return value</span></span>

<span data-ttu-id="1ddc9-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ddc9-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ddc9-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="1ddc9-118">Remarks</span></span>

<span data-ttu-id="1ddc9-119">Si un  nom nommé de forme de fond est présent dans le gabarit du document, le motif est appliqué en tant que motif de trait, motif de remplissage, flèche de début ou flèche de fin.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="1ddc9-120">Cette fonction renvoie toujours 254.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="1ddc9-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="1ddc9-121">Example</span></span>

<span data-ttu-id="1ddc9-122">USE("Voies ferrées")</span><span class="sxs-lookup"><span data-stu-id="1ddc9-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="1ddc9-123">Formate la forme en appliquant le motif de base intitulé Voies ferrées à la forme contenant la formule.</span><span class="sxs-lookup"><span data-stu-id="1ddc9-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

