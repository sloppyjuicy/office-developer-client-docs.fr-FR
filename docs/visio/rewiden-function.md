---
title: REWIDEN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Convertit une formule qui produit élargies codes de jeu de caractères codé sur un ou plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, les jeux de caractères spécifié à l’aide de codes de caractères 16 bits.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789485"
---
# <a name="rewiden-function"></a><span data-ttu-id="e4b1b-103">REWIDEN, fonction</span><span class="sxs-lookup"><span data-stu-id="e4b1b-103">REWIDEN Function</span></span>

<span data-ttu-id="e4b1b-104">Convertit une formule qui produit élargies codes de jeu de caractères codé sur un ou plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, les jeux de caractères spécifié à l’aide de codes de caractères 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e4b1b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4b1b-105">Syntax</span></span>

<span data-ttu-id="e4b1b-106">REWIDEN, (** *srcCharSet* **, ** *dstCharSet* **, ** *texte* **)</span><span class="sxs-lookup"><span data-stu-id="e4b1b-106">REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e4b1b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4b1b-107">Parameters</span></span>

|<span data-ttu-id="e4b1b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e4b1b-108">**Name**</span></span>|<span data-ttu-id="e4b1b-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e4b1b-109">**Required/Optional**</span></span>|<span data-ttu-id="e4b1b-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e4b1b-110">**Data Type**</span></span>|<span data-ttu-id="e4b1b-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e4b1b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e4b1b-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="e4b1b-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="e4b1b-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e4b1b-113">Required</span></span>  <br/> |<span data-ttu-id="e4b1b-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e4b1b-114">**String**</span></span> <br/> |<span data-ttu-id="e4b1b-115">Jeu de caractères du document source</span><span class="sxs-lookup"><span data-stu-id="e4b1b-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="e4b1b-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="e4b1b-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="e4b1b-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e4b1b-117">Required</span></span>  <br/> |<span data-ttu-id="e4b1b-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e4b1b-118">**String**</span></span> <br/> | <span data-ttu-id="e4b1b-119">Jeu de caractères du document de destination</span><span class="sxs-lookup"><span data-stu-id="e4b1b-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="e4b1b-120">_text_</span><span class="sxs-lookup"><span data-stu-id="e4b1b-120">_text_</span></span> <br/> |<span data-ttu-id="e4b1b-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e4b1b-121">Required</span></span>  <br/> |<span data-ttu-id="e4b1b-122">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e4b1b-122">**String**</span></span> <br/> |<span data-ttu-id="e4b1b-123">Texte à convertir</span><span class="sxs-lookup"><span data-stu-id="e4b1b-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4b1b-124">Note</span><span class="sxs-lookup"><span data-stu-id="e4b1b-124">Remarks</span></span>

<span data-ttu-id="e4b1b-p101">La fonction REWIDEN est utilisée pour la conversion automatique de documents Visio 2002 en documents Visio 2003. Une utilisation à une autre fin n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

