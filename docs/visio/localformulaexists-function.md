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
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788991"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="8bca7-103">LOCALFORMULAEXISTS, fonction</span><span class="sxs-lookup"><span data-stu-id="8bca7-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="8bca7-104">Indique si la cellule référencée contient une formule locale.</span><span class="sxs-lookup"><span data-stu-id="8bca7-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8bca7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bca7-105">Syntax</span></span>

<span data-ttu-id="8bca7-106">LOCALFORMULAEXISTS (** *cellref* **)</span><span class="sxs-lookup"><span data-stu-id="8bca7-106">LOCALFORMULAEXISTS (** *cellref* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8bca7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bca7-107">Parameters</span></span>

|<span data-ttu-id="8bca7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8bca7-108">**Name**</span></span>|<span data-ttu-id="8bca7-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8bca7-109">**Required/Optional**</span></span>|<span data-ttu-id="8bca7-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8bca7-110">**Data Type**</span></span>|<span data-ttu-id="8bca7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8bca7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8bca7-112">_CellRef_</span><span class="sxs-lookup"><span data-stu-id="8bca7-112">_cellref_</span></span> <br/> |<span data-ttu-id="8bca7-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8bca7-113">Required</span></span>  <br/> |<span data-ttu-id="8bca7-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bca7-114">**String**</span></span> <br/> | <span data-ttu-id="8bca7-115">Cellule dans laquelle vous voulez vérifier la présence d’une formule.</span><span class="sxs-lookup"><span data-stu-id="8bca7-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8bca7-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8bca7-116">Return value</span></span>

<span data-ttu-id="8bca7-117">Booléenne</span><span class="sxs-lookup"><span data-stu-id="8bca7-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bca7-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bca7-118">Remarks</span></span>

<span data-ttu-id="8bca7-119">La fonction LOCALFORMULAEXISTS renvoie 1 si la cellule contient une formule locale ; s’il n’y a pas de formule ou si la formule est héritée, elle renvoie 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="8bca7-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

