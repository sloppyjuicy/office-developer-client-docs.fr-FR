---
title: MSOTINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335195"
---
# <a name="msotint-function"></a><span data-ttu-id="cd603-103">Fonction MSOTINT</span><span class="sxs-lookup"><span data-stu-id="cd603-103">MSOTINT Function</span></span>

<span data-ttu-id="cd603-104">Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd603-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="cd603-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="cd603-105">Version Information</span></span>

<span data-ttu-id="cd603-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="cd603-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cd603-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd603-107">Syntax</span></span>

<span data-ttu-id="cd603-108">MSOTINT (\* \* *couleur* \* \*, \* \* *deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="cd603-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cd603-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd603-109">Parameters</span></span>

|<span data-ttu-id="cd603-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cd603-110">**Name**</span></span>|<span data-ttu-id="cd603-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="cd603-111">**Required/Optional**</span></span>|<span data-ttu-id="cd603-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="cd603-112">**Data Type**</span></span>|<span data-ttu-id="cd603-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="cd603-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cd603-114">_color_</span><span class="sxs-lookup"><span data-stu-id="cd603-114">_color_</span></span> <br/> |<span data-ttu-id="cd603-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cd603-115">Required</span></span>  <br/> |<span data-ttu-id="cd603-116">**RVB**</span><span class="sxs-lookup"><span data-stu-id="cd603-116">**RGB**</span></span> <br/> |<span data-ttu-id="cd603-117">Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.</span><span class="sxs-lookup"><span data-stu-id="cd603-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="cd603-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="cd603-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="cd603-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cd603-119">Required</span></span>  <br/> |<span data-ttu-id="cd603-120">**Entier**</span><span class="sxs-lookup"><span data-stu-id="cd603-120">**Integer**</span></span> <br/> |<span data-ttu-id="cd603-121">Pourcentage de changement vers blanc (-100%) ou noir (100%) de la valeur de _couleur_ .</span><span class="sxs-lookup"><span data-stu-id="cd603-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd603-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd603-122">Remarks</span></span>

<span data-ttu-id="cd603-123">Plus la valeur de _couleur_ est proche de blanc ou noir, plus la modification de la teinte générée par une valeur _deltaLum_ spécifique est faible.</span><span class="sxs-lookup"><span data-stu-id="cd603-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

