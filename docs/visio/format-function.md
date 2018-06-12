---
title: FORMAT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Renvoie le résultat d’expression sous forme de chaîne mise en forme selon formatpicture.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788690"
---
# <a name="format-function"></a><span data-ttu-id="c0b4c-103">FORMAT, fonction</span><span class="sxs-lookup"><span data-stu-id="c0b4c-103">FORMAT Function</span></span>

<span data-ttu-id="c0b4c-104">Renvoie le résultat _d’expression_ sous forme de chaîne mise en forme selon _formatpicture_.</span><span class="sxs-lookup"><span data-stu-id="c0b4c-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c0b4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0b4c-105">Syntax</span></span>

<span data-ttu-id="c0b4c-106">FORMAT (** *expression* **, « ** *formatpicture* ** »)</span><span class="sxs-lookup"><span data-stu-id="c0b4c-106">FORMAT(** *expression* **," ** *formatpicture* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0b4c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0b4c-107">Parameters</span></span>

|<span data-ttu-id="c0b4c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0b4c-108">**Name**</span></span>|<span data-ttu-id="c0b4c-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c0b4c-109">**Required/Optional**</span></span>|<span data-ttu-id="c0b4c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c0b4c-110">**Data Type**</span></span>|<span data-ttu-id="c0b4c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0b4c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0b4c-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="c0b4c-112">_expression_</span></span> <br/> |<span data-ttu-id="c0b4c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0b4c-113">Required</span></span>  <br/> |<span data-ttu-id="c0b4c-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="c0b4c-114">**String**</span></span> <br/> |<span data-ttu-id="c0b4c-115">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.</span><span class="sxs-lookup"><span data-stu-id="c0b4c-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="c0b4c-116">_formatPicture_</span><span class="sxs-lookup"><span data-stu-id="c0b4c-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="c0b4c-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0b4c-117">Required</span></span>  <br/> |<span data-ttu-id="c0b4c-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="c0b4c-118">**String**</span></span> <br/> |<span data-ttu-id="c0b4c-119">Modèle de format utilisé pour la mise en forme de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c0b4c-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c0b4c-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c0b4c-120">Return value</span></span>

<span data-ttu-id="c0b4c-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c0b4c-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0b4c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0b4c-122">Remarks</span></span>

<span data-ttu-id="c0b4c-123">Le type de l’expression et le type spécifié dans le modèle de format régissent le comportement de la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="c0b4c-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="c0b4c-124">Le _formatpicture_ doit être approprié pour le type d’expression.</span><span class="sxs-lookup"><span data-stu-id="c0b4c-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="c0b4c-125">Pour plus d’informations sur la spécification des modèles de format, voir [à propos des images de format](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="c0b4c-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="c0b4c-126">Renvoie une erreur si le résultat de _l’expression_ et le type attendu dans _formatpicture_ est de même nature ou s’il existe des erreurs de syntaxe dans _formatpicture_.</span><span class="sxs-lookup"><span data-stu-id="c0b4c-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="c0b4c-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="c0b4c-127">Example 1</span></span>

<span data-ttu-id="c0b4c-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="c0b4c-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="c0b4c-129">Renvoie « 0,250 cm ».</span><span class="sxs-lookup"><span data-stu-id="c0b4c-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c0b4c-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="c0b4c-130">Example 2</span></span>

<span data-ttu-id="c0b4c-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="c0b4c-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="c0b4c-132">Renvoie « 0,25 CM ».</span><span class="sxs-lookup"><span data-stu-id="c0b4c-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c0b4c-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="c0b4c-133">Example 3</span></span>

<span data-ttu-id="c0b4c-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="c0b4c-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="c0b4c-135">Renvoie « 0,3 cm ».</span><span class="sxs-lookup"><span data-stu-id="c0b4c-135">Returns "0.3 cm."</span></span>
  

