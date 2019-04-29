---
title: MSOSHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414493"
---
# <a name="msoshade-function"></a><span data-ttu-id="1050c-103">Fonction MSOSHADE</span><span class="sxs-lookup"><span data-stu-id="1050c-103">MSOSHADE Function</span></span>

<span data-ttu-id="1050c-104">Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="1050c-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="1050c-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="1050c-105">Version Information</span></span>

<span data-ttu-id="1050c-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="1050c-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1050c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1050c-107">Syntax</span></span>

<span data-ttu-id="1050c-108">MSOSHADE (\* \* *couleur* \* \*, \* \* *-deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1050c-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1050c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1050c-109">Parameters</span></span>

|<span data-ttu-id="1050c-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1050c-110">**Name**</span></span>|<span data-ttu-id="1050c-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="1050c-111">**Required/Optional**</span></span>|<span data-ttu-id="1050c-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="1050c-112">**Data Type**</span></span>|<span data-ttu-id="1050c-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="1050c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1050c-114">_color_</span><span class="sxs-lookup"><span data-stu-id="1050c-114">_color_</span></span> <br/> |<span data-ttu-id="1050c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1050c-115">Required</span></span>  <br/> |<span data-ttu-id="1050c-116">**RVB**</span><span class="sxs-lookup"><span data-stu-id="1050c-116">**RGB**</span></span> <br/> |<span data-ttu-id="1050c-117">Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.</span><span class="sxs-lookup"><span data-stu-id="1050c-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="1050c-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="1050c-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="1050c-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1050c-119">Required</span></span>  <br/> |<span data-ttu-id="1050c-120">**Entier**</span><span class="sxs-lookup"><span data-stu-id="1050c-120">**Integer**</span></span> <br/> |<span data-ttu-id="1050c-121">Pourcentage de changement vers blanc (-100%) ou noir (100%) de la valeur de _couleur_ .</span><span class="sxs-lookup"><span data-stu-id="1050c-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1050c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="1050c-122">Remarks</span></span>

<span data-ttu-id="1050c-123">Plus la valeur de _couleur_ est proche de blanc ou noir, plus le changement de dégradé généré par une valeur _-deltaLum_ spécifique est faible.</span><span class="sxs-lookup"><span data-stu-id="1050c-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

