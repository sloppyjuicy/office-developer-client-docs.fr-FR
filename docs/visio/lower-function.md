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
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789054"
---
# <a name="lower-function"></a><span data-ttu-id="6bb25-103">LOWER, fonction</span><span class="sxs-lookup"><span data-stu-id="6bb25-103">LOWER Function</span></span>

<span data-ttu-id="6bb25-104">Renvoie une chaîne convertie en minuscules.</span><span class="sxs-lookup"><span data-stu-id="6bb25-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6bb25-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bb25-105">Syntax</span></span>

<span data-ttu-id="6bb25-106">INFÉRIEUR (** *expression* **)</span><span class="sxs-lookup"><span data-stu-id="6bb25-106">LOWER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6bb25-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bb25-107">Parameters</span></span>

|<span data-ttu-id="6bb25-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6bb25-108">**Name**</span></span>|<span data-ttu-id="6bb25-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="6bb25-109">**Required/Optional**</span></span>|<span data-ttu-id="6bb25-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="6bb25-110">**Data Type**</span></span>|<span data-ttu-id="6bb25-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="6bb25-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6bb25-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="6bb25-112">_expression_</span></span> <br/> |<span data-ttu-id="6bb25-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6bb25-113">Required</span></span>  <br/> |<span data-ttu-id="6bb25-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="6bb25-114">**Varies**</span></span> <br/> | <span data-ttu-id="6bb25-115">Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en minuscules.</span><span class="sxs-lookup"><span data-stu-id="6bb25-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6bb25-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6bb25-116">Return value</span></span>

<span data-ttu-id="6bb25-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="6bb25-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6bb25-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="6bb25-118">Remarks</span></span>

<span data-ttu-id="6bb25-119">La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6bb25-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6bb25-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="6bb25-120">Example</span></span>

<span data-ttu-id="6bb25-121">LOWER("mAJ eT Min")</span><span class="sxs-lookup"><span data-stu-id="6bb25-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="6bb25-122">Renvoie « maj et min ».</span><span class="sxs-lookup"><span data-stu-id="6bb25-122">Returns "mixed case".</span></span> 
  

