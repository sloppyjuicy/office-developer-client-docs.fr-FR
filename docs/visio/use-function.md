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
description: Applique le motif de trait, le motif de remplissage ou l'extrémité de trait appelé nom à la forme lorsqu'elle est placée dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337148"
---
# <a name="use-function"></a><span data-ttu-id="e8b07-103">Fonction USE</span><span class="sxs-lookup"><span data-stu-id="e8b07-103">USE Function</span></span>

<span data-ttu-id="e8b07-104">Applique le motif de trait, le motif de remplissage ou l'extrémité de trait appelé _nom_ à la forme lorsqu'elle est placée dans la cellule LinePattern, FillPattern, BeginArrow ou EndArrow.</span><span class="sxs-lookup"><span data-stu-id="e8b07-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e8b07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8b07-105">Syntax</span></span>

<span data-ttu-id="e8b07-106">USE ("\* \* *Name* \* \*")</span><span class="sxs-lookup"><span data-stu-id="e8b07-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e8b07-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8b07-107">Parameters</span></span>

|<span data-ttu-id="e8b07-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e8b07-108">**Name**</span></span>|<span data-ttu-id="e8b07-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e8b07-109">**Required/Optional**</span></span>|<span data-ttu-id="e8b07-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e8b07-110">**Data Type**</span></span>|<span data-ttu-id="e8b07-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e8b07-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e8b07-112">_nom_</span><span class="sxs-lookup"><span data-stu-id="e8b07-112">_name_</span></span> <br/> |<span data-ttu-id="e8b07-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8b07-113">Required</span></span>  <br/> |<span data-ttu-id="e8b07-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e8b07-114">**String**</span></span> <br/> |<span data-ttu-id="e8b07-115">Chaîne correspondant à un nom de forme de base valide.</span><span class="sxs-lookup"><span data-stu-id="e8b07-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e8b07-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8b07-116">Return value</span></span>

<span data-ttu-id="e8b07-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8b07-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8b07-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8b07-118">Remarks</span></span>

<span data-ttu-id="e8b07-119">Si une forme de base nommée _nom_ est présente sur le gabarit de document du document, le motif est appliqué en tant que motif de trait, motif de remplissage, flèche de début ou flèche de fin.</span><span class="sxs-lookup"><span data-stu-id="e8b07-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="e8b07-120">Cette fonction renvoie toujours 254.</span><span class="sxs-lookup"><span data-stu-id="e8b07-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="e8b07-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="e8b07-121">Example</span></span>

<span data-ttu-id="e8b07-122">USE("Voies ferrées")</span><span class="sxs-lookup"><span data-stu-id="e8b07-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="e8b07-123">Formate la forme en appliquant le motif de base intitulé Voies ferrées à la forme contenant la formule.</span><span class="sxs-lookup"><span data-stu-id="e8b07-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

