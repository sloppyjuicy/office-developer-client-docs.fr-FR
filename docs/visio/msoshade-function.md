---
title: MSOSHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789157"
---
# <a name="msoshade-function"></a><span data-ttu-id="93d36-103">MSOSHADE, fonction</span><span class="sxs-lookup"><span data-stu-id="93d36-103">MSOSHADE Function</span></span>

<span data-ttu-id="93d36-104">Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="93d36-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="93d36-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="93d36-105">Version Information</span></span>

<span data-ttu-id="93d36-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="93d36-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="93d36-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93d36-107">Syntax</span></span>

<span data-ttu-id="93d36-108">MSOSHADE (** *couleur* **, ** *- deltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="93d36-108">MSOSHADE(** *color* **, ** *-deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="93d36-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93d36-109">Parameters</span></span>

|<span data-ttu-id="93d36-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="93d36-110">**Name**</span></span>|<span data-ttu-id="93d36-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="93d36-111">**Required/Optional**</span></span>|<span data-ttu-id="93d36-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="93d36-112">**Data Type**</span></span>|<span data-ttu-id="93d36-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="93d36-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="93d36-114">_color_</span><span class="sxs-lookup"><span data-stu-id="93d36-114">_color_</span></span> <br/> |<span data-ttu-id="93d36-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="93d36-115">Required</span></span>  <br/> |<span data-ttu-id="93d36-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="93d36-116">**RGB**</span></span> <br/> |<span data-ttu-id="93d36-117">Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.</span><span class="sxs-lookup"><span data-stu-id="93d36-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="93d36-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="93d36-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="93d36-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="93d36-119">Required</span></span>  <br/> |<span data-ttu-id="93d36-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="93d36-120">**Integer**</span></span> <br/> |<span data-ttu-id="93d36-121">Pourcentage de modification vers blanc (-100 %) ou noir (100 %) à partir de la valeur de _couleur_ .</span><span class="sxs-lookup"><span data-stu-id="93d36-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93d36-122">Note</span><span class="sxs-lookup"><span data-stu-id="93d36-122">Remarks</span></span>

<span data-ttu-id="93d36-123">Plus la valeur _color_ est blanc ou du noir, moins la modification de l’ombre qui est généré par une valeur spécifique _- deltaLum_ .</span><span class="sxs-lookup"><span data-stu-id="93d36-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

