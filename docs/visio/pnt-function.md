---
title: PNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Renvoie le point représenté par les coordonnées x et y en tant que valeur unique.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435711"
---
# <a name="pnt-function"></a><span data-ttu-id="01b3c-103">Fonction PNT</span><span class="sxs-lookup"><span data-stu-id="01b3c-103">PNT Function</span></span>

<span data-ttu-id="01b3c-104">Renvoie le point représenté par les coordonnées  _x_ et  _y_ en tant que valeur unique.</span><span class="sxs-lookup"><span data-stu-id="01b3c-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="01b3c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01b3c-105">Syntax</span></span>

<span data-ttu-id="01b3c-106">PNT(\*\* *x,y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="01b3c-106">PNT(\*\* *x,y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="01b3c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01b3c-107">Parameters</span></span>

|<span data-ttu-id="01b3c-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="01b3c-108">**Name**</span></span>|<span data-ttu-id="01b3c-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="01b3c-109">**Required/Optional**</span></span>|<span data-ttu-id="01b3c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="01b3c-110">**Data Type**</span></span>|<span data-ttu-id="01b3c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="01b3c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="01b3c-112">_x,y_</span><span class="sxs-lookup"><span data-stu-id="01b3c-112">_x,y_</span></span> <br/> |<span data-ttu-id="01b3c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="01b3c-113">Required</span></span>  <br/> |<span data-ttu-id="01b3c-114">**Number, Number**</span><span class="sxs-lookup"><span data-stu-id="01b3c-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="01b3c-115">Coordonnées du point dans le système de coordonnées de la forme actuelle</span><span class="sxs-lookup"><span data-stu-id="01b3c-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="01b3c-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="01b3c-116">Return value</span></span>

<span data-ttu-id="01b3c-117">Pointer</span><span class="sxs-lookup"><span data-stu-id="01b3c-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01b3c-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="01b3c-118">Remarks</span></span>

<span data-ttu-id="01b3c-119">La conversion de coordonnées en points vous permet de modifier la géométrie d’une forme sans avoir à manipuler les coordonnées  *x*  et  *y*  séparément.</span><span class="sxs-lookup"><span data-stu-id="01b3c-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="01b3c-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="01b3c-120">Example</span></span>

<span data-ttu-id="01b3c-121">PNT(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="01b3c-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="01b3c-122">Renvoie le point représenté par AxeX et AxeY.</span><span class="sxs-lookup"><span data-stu-id="01b3c-122">Returns the point represented by PinX and PinY.</span></span> 
  

