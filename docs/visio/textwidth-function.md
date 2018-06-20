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
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789873"
---
# <a name="textwidth-function"></a><span data-ttu-id="0d479-103">TEXTWIDTH, fonction</span><span class="sxs-lookup"><span data-stu-id="0d479-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="0d479-104">Renvoie la largeur du texte composé dans une forme.</span><span class="sxs-lookup"><span data-stu-id="0d479-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0d479-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d479-105">Syntax</span></span>

<span data-ttu-id="0d479-106">TEXTWIDTH (** shapename *! TheText* ** ** *[, largeurmaximale]* **)</span><span class="sxs-lookup"><span data-stu-id="0d479-106">TEXTWIDTH(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0d479-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d479-107">Parameters</span></span>

|<span data-ttu-id="0d479-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="0d479-108">**Name**</span></span>|<span data-ttu-id="0d479-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="0d479-109">**Required/Optional**</span></span>|<span data-ttu-id="0d479-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="0d479-110">**Data Type**</span></span>|<span data-ttu-id="0d479-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="0d479-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0d479-112">_l’argument shapename ! theText_</span><span class="sxs-lookup"><span data-stu-id="0d479-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="0d479-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0d479-113">Required</span></span>  <br/> |<span data-ttu-id="0d479-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d479-114">**String**</span></span> <br/> |<span data-ttu-id="0d479-115">Une référence à la cellule nommée TheText dans la forme cible.</span><span class="sxs-lookup"><span data-stu-id="0d479-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="0d479-116">_argument shapename !_</span><span class="sxs-lookup"><span data-stu-id="0d479-116">_shapename!_</span></span> <span data-ttu-id="0d479-117">est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.</span><span class="sxs-lookup"><span data-stu-id="0d479-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="0d479-118">_largeurmaximale_</span><span class="sxs-lookup"><span data-stu-id="0d479-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="0d479-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="0d479-119">Optional</span></span>  <br/> |<span data-ttu-id="0d479-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="0d479-120">**Numeric**</span></span> <br/> |<span data-ttu-id="0d479-121">Largeur maximale du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="0d479-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0d479-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0d479-122">Return value</span></span>

<span data-ttu-id="0d479-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0d479-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d479-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d479-124">Remarks</span></span>

<span data-ttu-id="0d479-125">La fonction TEXTWIDTH est couramment utilisée pour ajuster la largeur d’une forme au texte qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="0d479-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="0d479-126">Si _feuilleN !_</span><span class="sxs-lookup"><span data-stu-id="0d479-126">If  _sheetN!_</span></span> <span data-ttu-id="0d479-127">est omis, la forme par défaut est la forme active.</span><span class="sxs-lookup"><span data-stu-id="0d479-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="0d479-128">Si la _valeur largeurmaximale_ est indiquée, le résultat est la plus longue ligne de texte dans la _largeurmaximale_.</span><span class="sxs-lookup"><span data-stu-id="0d479-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="0d479-129">Si la _valeur largeurmaximale_ est omise, le résultat est la largeur totale du texte.</span><span class="sxs-lookup"><span data-stu-id="0d479-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0d479-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="0d479-130">Example</span></span>

<span data-ttu-id="0d479-131">TextWidth(TheText)</span><span class="sxs-lookup"><span data-stu-id="0d479-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="0d479-132">Renvoie la longueur totale du texte figurant dans la forme active.</span><span class="sxs-lookup"><span data-stu-id="0d479-132">Returns the total length of the text in the current shape.</span></span> 
  

