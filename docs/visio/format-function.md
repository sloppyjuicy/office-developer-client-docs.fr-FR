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
description: Renvoie le résultat d'expression sous la forme d'une chaîne mise en forme conformément à formatPicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339892"
---
# <a name="format-function"></a><span data-ttu-id="b2fbb-103">Fonction FORMAT</span><span class="sxs-lookup"><span data-stu-id="b2fbb-103">FORMAT Function</span></span>

<span data-ttu-id="b2fbb-104">Renvoie le résultat d' _expression_ sous la forme d'une chaîne mise en forme conformément à _formatPicture_.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b2fbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2fbb-105">Syntax</span></span>

<span data-ttu-id="b2fbb-106">FORMAT (\* \* *expression* \* *, "* \* *formatPicture* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b2fbb-106">FORMAT(\*\* *expression* \*\*," \*\* *formatpicture* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b2fbb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2fbb-107">Parameters</span></span>

|<span data-ttu-id="b2fbb-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b2fbb-108">**Name**</span></span>|<span data-ttu-id="b2fbb-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="b2fbb-109">**Required/Optional**</span></span>|<span data-ttu-id="b2fbb-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2fbb-110">**Data Type**</span></span>|<span data-ttu-id="b2fbb-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2fbb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b2fbb-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="b2fbb-112">_expression_</span></span> <br/> |<span data-ttu-id="b2fbb-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2fbb-113">Required</span></span>  <br/> |<span data-ttu-id="b2fbb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b2fbb-114">**String**</span></span> <br/> |<span data-ttu-id="b2fbb-115">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="b2fbb-116">_formatPicture_</span><span class="sxs-lookup"><span data-stu-id="b2fbb-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="b2fbb-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2fbb-117">Required</span></span>  <br/> |<span data-ttu-id="b2fbb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b2fbb-118">**String**</span></span> <br/> |<span data-ttu-id="b2fbb-119">Modèle de format utilisé pour la mise en forme de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b2fbb-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2fbb-120">Return value</span></span>

<span data-ttu-id="b2fbb-121">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2fbb-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2fbb-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2fbb-122">Remarks</span></span>

<span data-ttu-id="b2fbb-123">Le type de l’expression et celui indiqué dans le modèle de format régissent le comportement de la chaîne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="b2fbb-124">Le _formatPicture_ doit être approprié pour le type d'expression.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="b2fbb-125">Pour plus d'informations sur la spécification des images de format, voir [à propos de la mise en forme des images](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="b2fbb-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="b2fbb-126">Renvoie une erreur si le résultat d' _expression_ et le type attendu dans _formatPicture_ sont de même nature ou s'il existe des erreurs de syntaxe dans _formatPicture_.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="b2fbb-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b2fbb-127">Example 1</span></span>

<span data-ttu-id="b2fbb-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="b2fbb-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="b2fbb-129">Renvoie « 0,250 cm ».</span><span class="sxs-lookup"><span data-stu-id="b2fbb-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b2fbb-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b2fbb-130">Example 2</span></span>

<span data-ttu-id="b2fbb-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="b2fbb-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="b2fbb-132">Renvoie « 0,25 CM ».</span><span class="sxs-lookup"><span data-stu-id="b2fbb-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b2fbb-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="b2fbb-133">Example 3</span></span>

<span data-ttu-id="b2fbb-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="b2fbb-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="b2fbb-135">Renvoie « 0,3 cm ».</span><span class="sxs-lookup"><span data-stu-id="b2fbb-135">Returns "0.3 cm."</span></span>
  

