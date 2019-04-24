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
description: ConVertit une formule produisant des codes de caractères 16 bits qui sont des codes de jeu de caractères codés sur un octet ou sur plusieurs octets élargis en une chaîne de codes de caractères Unicode 16 bits, à l'aide des jeux de caractères spécifiés.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326767"
---
# <a name="rewiden-function"></a><span data-ttu-id="485d3-103">Fonction REWIDEN</span><span class="sxs-lookup"><span data-stu-id="485d3-103">REWIDEN Function</span></span>

<span data-ttu-id="485d3-104">ConVertit une formule produisant des codes de caractères 16 bits qui sont des codes de jeu de caractères codés sur un octet ou sur plusieurs octets élargis en une chaîne de codes de caractères Unicode 16 bits, à l'aide des jeux de caractères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="485d3-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="485d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="485d3-105">Syntax</span></span>

<span data-ttu-id="485d3-106">ReLARGESn (\* \* *srcCharSet* \* \*, \* \* *dstCharSet* \* \*, \* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="485d3-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="485d3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="485d3-107">Parameters</span></span>

|<span data-ttu-id="485d3-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="485d3-108">**Name**</span></span>|<span data-ttu-id="485d3-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="485d3-109">**Required/Optional**</span></span>|<span data-ttu-id="485d3-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="485d3-110">**Data Type**</span></span>|<span data-ttu-id="485d3-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="485d3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="485d3-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="485d3-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="485d3-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="485d3-113">Required</span></span>  <br/> |<span data-ttu-id="485d3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="485d3-114">**String**</span></span> <br/> |<span data-ttu-id="485d3-115">Jeu de caractères du document source</span><span class="sxs-lookup"><span data-stu-id="485d3-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="485d3-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="485d3-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="485d3-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="485d3-117">Required</span></span>  <br/> |<span data-ttu-id="485d3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="485d3-118">**String**</span></span> <br/> | <span data-ttu-id="485d3-119">Jeu de caractères du document de destination</span><span class="sxs-lookup"><span data-stu-id="485d3-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="485d3-120">_text_</span><span class="sxs-lookup"><span data-stu-id="485d3-120">_text_</span></span> <br/> |<span data-ttu-id="485d3-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="485d3-121">Required</span></span>  <br/> |<span data-ttu-id="485d3-122">**String**</span><span class="sxs-lookup"><span data-stu-id="485d3-122">**String**</span></span> <br/> |<span data-ttu-id="485d3-123">Texte à convertir</span><span class="sxs-lookup"><span data-stu-id="485d3-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="485d3-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="485d3-124">Remarks</span></span>

<span data-ttu-id="485d3-p101">La fonction REWIDEN est utilisée pour la conversion automatique de documents Visio 2002 en documents Visio 2003. Une utilisation à une autre fin n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="485d3-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

