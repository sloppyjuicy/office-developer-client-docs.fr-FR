---
title: LOWER, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Renvoie une chaîne convertie en minuscules.
ms.openlocfilehash: 275e5cc40bed5c3ca7d6f40b0882f523334611c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421241"
---
# <a name="lower-function"></a><span data-ttu-id="f816d-103">Fonction LOWER</span><span class="sxs-lookup"><span data-stu-id="f816d-103">LOWER Function</span></span>

<span data-ttu-id="f816d-104">Renvoie une chaîne convertie en minuscules.</span><span class="sxs-lookup"><span data-stu-id="f816d-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f816d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f816d-105">Syntax</span></span>

<span data-ttu-id="f816d-106">LOWER (\* \* *expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f816d-106">LOWER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f816d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f816d-107">Parameters</span></span>

|<span data-ttu-id="f816d-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f816d-108">**Name**</span></span>|<span data-ttu-id="f816d-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f816d-109">**Required/Optional**</span></span>|<span data-ttu-id="f816d-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f816d-110">**Data Type**</span></span>|<span data-ttu-id="f816d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f816d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f816d-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="f816d-112">_expression_</span></span> <br/> |<span data-ttu-id="f816d-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f816d-113">Required</span></span>  <br/> |<span data-ttu-id="f816d-114">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="f816d-114">**Varies**</span></span> <br/> | <span data-ttu-id="f816d-115">Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en minuscules.</span><span class="sxs-lookup"><span data-stu-id="f816d-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f816d-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f816d-116">Return value</span></span>

<span data-ttu-id="f816d-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f816d-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f816d-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="f816d-118">Remarks</span></span>

<span data-ttu-id="f816d-119">La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f816d-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f816d-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="f816d-120">Example</span></span>

<span data-ttu-id="f816d-121">LOWER("mAJ eT Min")</span><span class="sxs-lookup"><span data-stu-id="f816d-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="f816d-122">Renvoie « maj et min ».</span><span class="sxs-lookup"><span data-stu-id="f816d-122">Returns "mixed case".</span></span> 
  

