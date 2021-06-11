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
description: Convertit une formule qui produit des codes de caractères 16 bits qui sont élargis de codes de jeu de caractères codés sur un octet ou sur plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, à l’aide des jeux de caractères spécifiés.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405211"
---
# <a name="rewiden-function"></a><span data-ttu-id="9a55f-103">Fonction REWIDEN</span><span class="sxs-lookup"><span data-stu-id="9a55f-103">REWIDEN Function</span></span>

<span data-ttu-id="9a55f-104">Convertit une formule qui produit des codes de caractères 16 bits qui sont élargis de codes de jeu de caractères codés sur un octet ou sur plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, à l’aide des jeux de caractères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9a55f-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9a55f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a55f-105">Syntax</span></span>

<span data-ttu-id="9a55f-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="9a55f-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9a55f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a55f-107">Parameters</span></span>

|<span data-ttu-id="9a55f-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9a55f-108">**Name**</span></span>|<span data-ttu-id="9a55f-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9a55f-109">**Required/Optional**</span></span>|<span data-ttu-id="9a55f-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9a55f-110">**Data Type**</span></span>|<span data-ttu-id="9a55f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a55f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9a55f-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="9a55f-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="9a55f-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9a55f-113">Required</span></span>  <br/> |<span data-ttu-id="9a55f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9a55f-114">**String**</span></span> <br/> |<span data-ttu-id="9a55f-115">Jeu de caractères du document source</span><span class="sxs-lookup"><span data-stu-id="9a55f-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="9a55f-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="9a55f-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="9a55f-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9a55f-117">Required</span></span>  <br/> |<span data-ttu-id="9a55f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9a55f-118">**String**</span></span> <br/> | <span data-ttu-id="9a55f-119">Jeu de caractères du document de destination</span><span class="sxs-lookup"><span data-stu-id="9a55f-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="9a55f-120">_text_</span><span class="sxs-lookup"><span data-stu-id="9a55f-120">_text_</span></span> <br/> |<span data-ttu-id="9a55f-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9a55f-121">Required</span></span>  <br/> |<span data-ttu-id="9a55f-122">**String**</span><span class="sxs-lookup"><span data-stu-id="9a55f-122">**String**</span></span> <br/> |<span data-ttu-id="9a55f-123">Texte à convertir</span><span class="sxs-lookup"><span data-stu-id="9a55f-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a55f-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a55f-124">Remarks</span></span>

<span data-ttu-id="9a55f-p101">La fonction REWIDEN est utilisée pour la conversion automatique de documents Visio 2002 en documents Visio 2003. Une utilisation à une autre fin n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="9a55f-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

