---
title: LOCTOPAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Renvoie un point transformé dans les coordonnées parent dans le système de coordonnées de destination.
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439981"
---
# <a name="loctopar-function"></a><span data-ttu-id="0aacb-103">Fonction LOCTOPAR</span><span class="sxs-lookup"><span data-stu-id="0aacb-103">LOCTOPAR Function</span></span>

<span data-ttu-id="0aacb-104">Renvoie un point transformé dans les coordonnées parent dans le système de coordonnées de destination.</span><span class="sxs-lookup"><span data-stu-id="0aacb-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0aacb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aacb-105">Syntax</span></span>

<span data-ttu-id="0aacb-106">LOCTOPAR(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span><span class="sxs-lookup"><span data-stu-id="0aacb-106">LOCTOPAR(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0aacb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aacb-107">Parameters</span></span>

|<span data-ttu-id="0aacb-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0aacb-108">**Name**</span></span>|<span data-ttu-id="0aacb-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="0aacb-109">**Required/Optional**</span></span>|<span data-ttu-id="0aacb-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="0aacb-110">**Data Type**</span></span>|<span data-ttu-id="0aacb-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="0aacb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0aacb-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="0aacb-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="0aacb-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0aacb-113">Required</span></span>  <br/> |<span data-ttu-id="0aacb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0aacb-114">**String**</span></span> <br/> | <span data-ttu-id="0aacb-115">Point en coordonnées locales du système de coordonnées source</span><span class="sxs-lookup"><span data-stu-id="0aacb-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="0aacb-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="0aacb-116">_srcRef_</span></span> <br/> |<span data-ttu-id="0aacb-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0aacb-117">Required</span></span>  <br/> |<span data-ttu-id="0aacb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="0aacb-118">**String**</span></span> <br/> | <span data-ttu-id="0aacb-119">Référence à une cellule de l’objet source</span><span class="sxs-lookup"><span data-stu-id="0aacb-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="0aacb-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="0aacb-120">_dstRef_</span></span> <br/> |<span data-ttu-id="0aacb-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0aacb-121">Required</span></span>  <br/> |<span data-ttu-id="0aacb-122">**String**</span><span class="sxs-lookup"><span data-stu-id="0aacb-122">**String**</span></span> <br/> | <span data-ttu-id="0aacb-123">Référence à une cellule de l’objet cible</span><span class="sxs-lookup"><span data-stu-id="0aacb-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0aacb-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0aacb-124">Return value</span></span>

<span data-ttu-id="0aacb-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0aacb-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0aacb-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="0aacb-126">Remarks</span></span>

<span data-ttu-id="0aacb-p101">La fonction LOCTOPAR convertit un point des coordonnées locales dans une forme source en coordonnées parent de la forme de destination. Vous pouvez utiliser la fonction LOCTOPAR pour définir des coordonnées parent dans les cellules d’une forme, comme PinX, PinY, BeginX et BeginY, en utilisant un point d’un autre système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="0aacb-p101">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape. You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="0aacb-p102">Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="0aacb-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="0aacb-131">Les coordonnées source et cible doivent se trouver sur la même page.</span><span class="sxs-lookup"><span data-stu-id="0aacb-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="0aacb-132">Si la destination est une page qui n’a pas de parent, le résultat est exprimé dans les coordonnées locales de la page.</span><span class="sxs-lookup"><span data-stu-id="0aacb-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0aacb-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="0aacb-133">Example</span></span>

<span data-ttu-id="0aacb-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width; Feuille.4!Width)</span><span class="sxs-lookup"><span data-stu-id="0aacb-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="0aacb-135">Convertit les coordonnées de l’axe local de la forme associée à la formule en coordonnées parent de Feuille.4.</span><span class="sxs-lookup"><span data-stu-id="0aacb-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

