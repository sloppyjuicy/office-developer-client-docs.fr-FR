---
title: LOCALFORMULAEXISTS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Indique si la cellule référencée contient une formule locale.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433289"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="f7709-103">Fonction LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="f7709-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="f7709-104">Indique si la cellule référencée contient une formule locale.</span><span class="sxs-lookup"><span data-stu-id="f7709-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f7709-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7709-105">Syntax</span></span>

<span data-ttu-id="f7709-106">LOCALFORMULAEXISTS (\* \* *CellRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f7709-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f7709-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7709-107">Parameters</span></span>

|<span data-ttu-id="f7709-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f7709-108">**Name**</span></span>|<span data-ttu-id="f7709-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f7709-109">**Required/Optional**</span></span>|<span data-ttu-id="f7709-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f7709-110">**Data Type**</span></span>|<span data-ttu-id="f7709-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f7709-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f7709-112">_CellRef_</span><span class="sxs-lookup"><span data-stu-id="f7709-112">_cellref_</span></span> <br/> |<span data-ttu-id="f7709-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7709-113">Required</span></span>  <br/> |<span data-ttu-id="f7709-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f7709-114">**String**</span></span> <br/> | <span data-ttu-id="f7709-115">Cellule dans laquelle vous voulez vérifier la présence d’une formule.</span><span class="sxs-lookup"><span data-stu-id="f7709-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f7709-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f7709-116">Return value</span></span>

<span data-ttu-id="f7709-117">Booléen</span><span class="sxs-lookup"><span data-stu-id="f7709-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7709-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7709-118">Remarks</span></span>

<span data-ttu-id="f7709-119">La fonction LOCALFORMULAEXISTS renvoie 1 si la cellule contient une formule locale ; s’il n’y a pas de formule ou si la formule est héritée, elle renvoie 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="f7709-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

