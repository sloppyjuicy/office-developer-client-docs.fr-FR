---
title: TEXTHEIGHT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse maximumwidth.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427408"
---
# <a name="textheight-function"></a><span data-ttu-id="6ceb7-103">Fonction TEXTHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6ceb7-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="6ceb7-104">Renvoie la hauteur du texte composé dans une forme où aucune ligne de texte ne dépasse  _maximumwidth_.</span><span class="sxs-lookup"><span data-stu-id="6ceb7-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6ceb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ceb7-105">Syntax</span></span>

<span data-ttu-id="6ceb7-106">TEXTHEIGHT(\*\* *shapename! TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6ceb7-106">TEXTHEIGHT(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6ceb7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ceb7-107">Parameters</span></span>

|<span data-ttu-id="6ceb7-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6ceb7-108">**Name**</span></span>|<span data-ttu-id="6ceb7-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="6ceb7-109">**Required/Optional**</span></span>|<span data-ttu-id="6ceb7-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="6ceb7-110">**Data Type**</span></span>|<span data-ttu-id="6ceb7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="6ceb7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6ceb7-112">_shapename!theText_</span><span class="sxs-lookup"><span data-stu-id="6ceb7-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="6ceb7-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6ceb7-113">Required</span></span>  <br/> |<span data-ttu-id="6ceb7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6ceb7-114">**String**</span></span> <br/> |<span data-ttu-id="6ceb7-115">Référence à la cellule nommée TheText dans la forme cible.</span><span class="sxs-lookup"><span data-stu-id="6ceb7-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="6ceb7-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="6ceb7-116">_shapename!_</span></span> <span data-ttu-id="6ceb7-117">est le nom de la forme à partir de laquelle vous souhaitez récupérer le texte.</span><span class="sxs-lookup"><span data-stu-id="6ceb7-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="6ceb7-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="6ceb7-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="6ceb7-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="6ceb7-119">Optional</span></span>  <br/> |<span data-ttu-id="6ceb7-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="6ceb7-120">**Numeric**</span></span> <br/> |<span data-ttu-id="6ceb7-121">Largeur maximale du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="6ceb7-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6ceb7-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ceb7-122">Return value</span></span>

<span data-ttu-id="6ceb7-123">Chaîne</span><span class="sxs-lookup"><span data-stu-id="6ceb7-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ceb7-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ceb7-124">Remarks</span></span>

<span data-ttu-id="6ceb7-p102">La valeur renvoyée comprend la hauteur du texte, ainsi que l’espace précédant et suivant le texte, l’interligne et les marges haut et bas du bloc de texte. Cette fonction est couramment utilisée pour ajuster la hauteur d’une forme au texte qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="6ceb7-p102">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins. This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="6ceb7-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ceb7-127">Example</span></span>

<span data-ttu-id="6ceb7-128">TEXTHEIGHT(LeTexte,(Largeur - 12,7 mm))</span><span class="sxs-lookup"><span data-stu-id="6ceb7-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="6ceb7-129">Renvoie la hauteur du texte développé, lorsque ce dernier est ramené à la largeur de la forme moins 12,7 mm.</span><span class="sxs-lookup"><span data-stu-id="6ceb7-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

