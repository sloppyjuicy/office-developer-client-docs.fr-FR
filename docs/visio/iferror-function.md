---
title: IFERROR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: Renvoie le résultat évalué d'une expression primaire, si elle n'évalue pas une erreur. Sinon, cette fonction renvoie le résultat évalué d’une autre expression.
ms.openlocfilehash: 7b9b42b5c7e7053bae862ddadf17e65015d8ecc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431175"
---
# <a name="iferror-function"></a><span data-ttu-id="d56be-104">Fonction SIERROR</span><span class="sxs-lookup"><span data-stu-id="d56be-104">IFERROR Function</span></span>

<span data-ttu-id="d56be-105">Renvoie le résultat évalué d'une expression primaire, si elle n'évalue pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="d56be-105">Returns the evaluated result of a primary expression, if it does not evaluate to an error.</span></span> <span data-ttu-id="d56be-106">Sinon, cette fonction renvoie le résultat évalué d’une autre expression.</span><span class="sxs-lookup"><span data-stu-id="d56be-106">Otherwise, returns the evaluated result of an alternate expression.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d56be-107">Informations de version</span><span class="sxs-lookup"><span data-stu-id="d56be-107">Version Information</span></span>

<span data-ttu-id="d56be-108">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d56be-108">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d56be-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d56be-109">Syntax</span></span>

<span data-ttu-id="d56be-110">IFERROR (\* \* *expression primaire* \* \*, \* \* *expression de remplacement* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d56be-110">IFERROR(\*\* *primary expression* \*\*, \*\* *alternate expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d56be-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d56be-111">Parameters</span></span>

|<span data-ttu-id="d56be-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d56be-112">**Name**</span></span>|<span data-ttu-id="d56be-113">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d56be-113">**Required/Optional**</span></span>|<span data-ttu-id="d56be-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d56be-114">**Data Type**</span></span>|<span data-ttu-id="d56be-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="d56be-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d56be-116">_expression primaire_</span><span class="sxs-lookup"><span data-stu-id="d56be-116">_primary expression_</span></span> <br/> |<span data-ttu-id="d56be-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d56be-117">Required</span></span>  <br/> |<span data-ttu-id="d56be-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d56be-118">**String**</span></span> <br/> |<span data-ttu-id="d56be-119">Première expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="d56be-119">The first expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="d56be-120">_expression de substitution_</span><span class="sxs-lookup"><span data-stu-id="d56be-120">_alternate expression_</span></span> <br/> |<span data-ttu-id="d56be-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d56be-121">Required</span></span>  <br/> |<span data-ttu-id="d56be-122">**String**</span><span class="sxs-lookup"><span data-stu-id="d56be-122">**String**</span></span> <br/> |<span data-ttu-id="d56be-123">Autre expression à évaluer si la première expression évalue une erreur.</span><span class="sxs-lookup"><span data-stu-id="d56be-123">The alternate expression to evaluate if the primary expression evaluates to an error.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d56be-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d56be-124">Return value</span></span>

<span data-ttu-id="d56be-125">Variables</span><span class="sxs-lookup"><span data-stu-id="d56be-125">Varies</span></span>
  

