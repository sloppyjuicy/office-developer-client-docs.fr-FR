---
title: PATHSEGMENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Renvoie le numéro de segment de base 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789232"
---
# <a name="pathsegment-function"></a><span data-ttu-id="a7de2-103">PATHSEGMENT, fonction</span><span class="sxs-lookup"><span data-stu-id="a7de2-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="a7de2-104">Renvoie le numéro de segment de base 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7de2-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a7de2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7de2-105">Syntax</span></span>

<span data-ttu-id="a7de2-106">PATHSEGMENT (** *section* **, ** *voyage* **)</span><span class="sxs-lookup"><span data-stu-id="a7de2-106">PATHSEGMENT(** *section* **, ** *travel* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a7de2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7de2-107">Parameters</span></span>

|<span data-ttu-id="a7de2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a7de2-108">**Name**</span></span>|<span data-ttu-id="a7de2-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a7de2-109">**Required/Optional**</span></span>|<span data-ttu-id="a7de2-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a7de2-110">**Data Type**</span></span>|<span data-ttu-id="a7de2-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a7de2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a7de2-112">_section_</span><span class="sxs-lookup"><span data-stu-id="a7de2-112">_section_</span></span> <br/> |<span data-ttu-id="a7de2-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a7de2-113">Required</span></span>  <br/> |<span data-ttu-id="a7de2-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7de2-114">**String**</span></span> <br/> |<span data-ttu-id="a7de2-115">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="a7de2-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="a7de2-116">_frais de déplacement_</span><span class="sxs-lookup"><span data-stu-id="a7de2-116">_travel_</span></span> <br/> |<span data-ttu-id="a7de2-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a7de2-117">Required</span></span>  <br/> |<span data-ttu-id="a7de2-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="a7de2-118">**Double**</span></span> <br/> |<span data-ttu-id="a7de2-p101">Pourcentage du chemin parcouru du point de début au point de fin. La valeur doit être comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="a7de2-p101">The percentage of the path traversed, from the begin point to the end point. Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a7de2-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a7de2-121">Return value</span></span>

<span data-ttu-id="a7de2-122">Entier</span><span class="sxs-lookup"><span data-stu-id="a7de2-122">Integer</span></span>
  

