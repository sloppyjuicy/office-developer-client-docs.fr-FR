---
title: MSOTINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789186"
---
# <a name="msotint-function"></a><span data-ttu-id="38028-103">MSOTINT, fonction</span><span class="sxs-lookup"><span data-stu-id="38028-103">MSOTINT Function</span></span>

<span data-ttu-id="38028-104">Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="38028-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="38028-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="38028-105">Version Information</span></span>

<span data-ttu-id="38028-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="38028-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="38028-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38028-107">Syntax</span></span>

<span data-ttu-id="38028-108">MSOTINT (** *couleur* **, ** *deltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="38028-108">MSOTINT(** *color* **, ** *deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="38028-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38028-109">Parameters</span></span>

|<span data-ttu-id="38028-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="38028-110">**Name**</span></span>|<span data-ttu-id="38028-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="38028-111">**Required/Optional**</span></span>|<span data-ttu-id="38028-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="38028-112">**Data Type**</span></span>|<span data-ttu-id="38028-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="38028-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="38028-114">_color_</span><span class="sxs-lookup"><span data-stu-id="38028-114">_color_</span></span> <br/> |<span data-ttu-id="38028-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="38028-115">Required</span></span>  <br/> |<span data-ttu-id="38028-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="38028-116">**RGB**</span></span> <br/> |<span data-ttu-id="38028-117">Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.</span><span class="sxs-lookup"><span data-stu-id="38028-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="38028-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="38028-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="38028-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="38028-119">Required</span></span>  <br/> |<span data-ttu-id="38028-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="38028-120">**Integer**</span></span> <br/> |<span data-ttu-id="38028-121">Pourcentage de modification vers blanc (-100 %) ou noir (100 %) à partir de la valeur de _couleur_ .</span><span class="sxs-lookup"><span data-stu-id="38028-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38028-122">Note</span><span class="sxs-lookup"><span data-stu-id="38028-122">Remarks</span></span>

<span data-ttu-id="38028-123">Plus la valeur _color_ est blanc ou du noir, moins la modification de la teinte générée par une valeur spécifique _deltaLum_ .</span><span class="sxs-lookup"><span data-stu-id="38028-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

