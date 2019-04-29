---
title: UPPER, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
localization_priority: Normal
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: Renvoie une chaîne convertie en majuscules.
ms.openlocfilehash: b88958526bfb5e08839077217759f7ffb50151b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415144"
---
# <a name="upper-function"></a><span data-ttu-id="7b3c4-103">Fonction UPPER</span><span class="sxs-lookup"><span data-stu-id="7b3c4-103">UPPER Function</span></span>

<span data-ttu-id="7b3c4-104">Renvoie une chaîne convertie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="7b3c4-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7b3c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b3c4-105">Syntax</span></span>

<span data-ttu-id="7b3c4-106">MAJUSCULE (\* \* *expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7b3c4-106">UPPER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7b3c4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b3c4-107">Parameters</span></span>

|<span data-ttu-id="7b3c4-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-108">**Name**</span></span>|<span data-ttu-id="7b3c4-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-109">**Required/Optional**</span></span>|<span data-ttu-id="7b3c4-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-110">**Data Type**</span></span>|<span data-ttu-id="7b3c4-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7b3c4-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="7b3c4-112">_expression_</span></span> <br/> |<span data-ttu-id="7b3c4-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7b3c4-113">Required</span></span>  <br/> |<span data-ttu-id="7b3c4-114">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-114">**Varies**</span></span> <br/> | <span data-ttu-id="7b3c4-115">Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="7b3c4-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b3c4-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b3c4-116">Remarks</span></span>

<span data-ttu-id="7b3c4-117">La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b3c4-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7b3c4-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="7b3c4-118">Example</span></span>

<span data-ttu-id="7b3c4-119">UPPER("mAJ eT Min")</span><span class="sxs-lookup"><span data-stu-id="7b3c4-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="7b3c4-120">Renvoie "MAJ ET MIN".</span><span class="sxs-lookup"><span data-stu-id="7b3c4-120">Returns "MIXED CASE".</span></span> 
  

