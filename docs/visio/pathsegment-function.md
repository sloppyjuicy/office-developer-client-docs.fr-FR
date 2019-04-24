---
title: PATHSEGMENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d'accès spécifié.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344449"
---
# <a name="pathsegment-function"></a><span data-ttu-id="5583a-103">Fonction PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="5583a-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="5583a-104">Renvoie le numéro de segment basé sur 1 à la marque de pourcentage spécifiée le long du chemin d'accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="5583a-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5583a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5583a-105">Syntax</span></span>

<span data-ttu-id="5583a-106">PATHSEGMENT (\* \* *section* \* \*, \* \* *voyages* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5583a-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5583a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5583a-107">Parameters</span></span>

|<span data-ttu-id="5583a-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5583a-108">**Name**</span></span>|<span data-ttu-id="5583a-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="5583a-109">**Required/Optional**</span></span>|<span data-ttu-id="5583a-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="5583a-110">**Data Type**</span></span>|<span data-ttu-id="5583a-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="5583a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5583a-112">_section_</span><span class="sxs-lookup"><span data-stu-id="5583a-112">_section_</span></span> <br/> |<span data-ttu-id="5583a-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5583a-113">Required</span></span>  <br/> |<span data-ttu-id="5583a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5583a-114">**String**</span></span> <br/> |<span data-ttu-id="5583a-115">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="5583a-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="5583a-116">_poche_</span><span class="sxs-lookup"><span data-stu-id="5583a-116">_travel_</span></span> <br/> |<span data-ttu-id="5583a-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5583a-117">Required</span></span>  <br/> |<span data-ttu-id="5583a-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="5583a-118">**Double**</span></span> <br/> |<span data-ttu-id="5583a-119">Pourcentage du chemin parcouru du point de début au point de fin.</span><span class="sxs-lookup"><span data-stu-id="5583a-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="5583a-120">La valeur doit être comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="5583a-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5583a-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5583a-121">Return value</span></span>

<span data-ttu-id="5583a-122">Entier</span><span class="sxs-lookup"><span data-stu-id="5583a-122">Integer</span></span>
  

