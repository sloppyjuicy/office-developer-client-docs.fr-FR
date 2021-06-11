---
title: TEXTWIDTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Renvoie la largeur du texte composé dans une forme.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422032"
---
# <a name="textwidth-function"></a><span data-ttu-id="8c7b5-103">Fonction TEXTWIDTH</span><span class="sxs-lookup"><span data-stu-id="8c7b5-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="8c7b5-104">Renvoie la largeur du texte composé dans une forme.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8c7b5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c7b5-105">Syntax</span></span>

<span data-ttu-id="8c7b5-106">TEXTWIDTH(\*\* *shapename! TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8c7b5-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c7b5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c7b5-107">Parameters</span></span>

|<span data-ttu-id="8c7b5-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8c7b5-108">**Name**</span></span>|<span data-ttu-id="8c7b5-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8c7b5-109">**Required/Optional**</span></span>|<span data-ttu-id="8c7b5-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8c7b5-110">**Data Type**</span></span>|<span data-ttu-id="8c7b5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8c7b5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c7b5-112">_shapename!theText_</span><span class="sxs-lookup"><span data-stu-id="8c7b5-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="8c7b5-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c7b5-113">Required</span></span>  <br/> |<span data-ttu-id="8c7b5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8c7b5-114">**String**</span></span> <br/> |<span data-ttu-id="8c7b5-115">Référence à la cellule nommée TheText dans la forme cible.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="8c7b5-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="8c7b5-116">_shapename!_</span></span> <span data-ttu-id="8c7b5-117">est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="8c7b5-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="8c7b5-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="8c7b5-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="8c7b5-119">Optional</span></span>  <br/> |<span data-ttu-id="8c7b5-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8c7b5-120">**Numeric**</span></span> <br/> |<span data-ttu-id="8c7b5-121">Largeur maximale du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8c7b5-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8c7b5-122">Return value</span></span>

<span data-ttu-id="8c7b5-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8c7b5-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c7b5-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="8c7b5-124">Remarks</span></span>

<span data-ttu-id="8c7b5-125">La fonction TEXTWIDTH est couramment utilisée pour ajuster la largeur d’une forme au texte qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="8c7b5-126">If  _sheetN!_</span><span class="sxs-lookup"><span data-stu-id="8c7b5-126">If  _sheetN!_</span></span> <span data-ttu-id="8c7b5-127">est omis, la forme par défaut est la forme actuelle.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="8c7b5-128">Si  _maximumwidth est_ spécifié, le résultat est la ligne de texte la plus longue qui s’adapte  _à maximumwidth_.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="8c7b5-129">Si  _la valeur maximumwidth_ est omise, le résultat est la largeur totale du texte.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8c7b5-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="8c7b5-130">Example</span></span>

<span data-ttu-id="8c7b5-131">TEXTWIDTH(TheText)</span><span class="sxs-lookup"><span data-stu-id="8c7b5-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="8c7b5-132">Renvoie la longueur totale du texte dans la forme actuelle.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-132">Returns the total length of the text in the current shape.</span></span> 
  

