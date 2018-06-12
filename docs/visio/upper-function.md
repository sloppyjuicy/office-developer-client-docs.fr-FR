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
ms.openlocfilehash: df8250ef634b04cb19cbb4e120bd02eb77531a82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789974"
---
# <a name="upper-function"></a><span data-ttu-id="3cfef-103">UPPER, fonction</span><span class="sxs-lookup"><span data-stu-id="3cfef-103">UPPER Function</span></span>

<span data-ttu-id="3cfef-104">Renvoie une chaîne convertie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="3cfef-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3cfef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cfef-105">Syntax</span></span>

<span data-ttu-id="3cfef-106">SUPÉRIEUR (** *expression* **)</span><span class="sxs-lookup"><span data-stu-id="3cfef-106">UPPER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3cfef-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cfef-107">Parameters</span></span>

|<span data-ttu-id="3cfef-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3cfef-108">**Name**</span></span>|<span data-ttu-id="3cfef-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3cfef-109">**Required/Optional**</span></span>|<span data-ttu-id="3cfef-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3cfef-110">**Data Type**</span></span>|<span data-ttu-id="3cfef-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="3cfef-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3cfef-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="3cfef-112">_expression_</span></span> <br/> |<span data-ttu-id="3cfef-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3cfef-113">Required</span></span>  <br/> |<span data-ttu-id="3cfef-114">**Varie**</span><span class="sxs-lookup"><span data-stu-id="3cfef-114">**Varies**</span></span> <br/> | <span data-ttu-id="3cfef-115">Chaîne, référence de cellule ou expression ; le résultat est converti en une chaîne à son tour convertie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="3cfef-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cfef-116">Note</span><span class="sxs-lookup"><span data-stu-id="3cfef-116">Remarks</span></span>

<span data-ttu-id="3cfef-117">La conversion dépend des paramètres régionaux et est basée sur les paramètres actuels de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3cfef-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3cfef-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="3cfef-118">Example</span></span>

<span data-ttu-id="3cfef-119">UPPER("mAJ eT Min")</span><span class="sxs-lookup"><span data-stu-id="3cfef-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="3cfef-120">Renvoie "MAJ ET MIN".</span><span class="sxs-lookup"><span data-stu-id="3cfef-120">Returns "MIXED CASE".</span></span> 
  

