---
title: BITAND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans binarynumber1 et binarynumber2 est 1. Dans le cas contraire, le bit prend la valeur 0.
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409726"
---
# <a name="bitand-function"></a><span data-ttu-id="f9bc7-104">Fonction BITAND</span><span class="sxs-lookup"><span data-stu-id="f9bc7-104">BITAND Function</span></span>

<span data-ttu-id="f9bc7-105">Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans binarynumber1 et binarynumber2 est 1.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="f9bc7-106">Dans le cas contraire, le bit prend la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f9bc7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9bc7-107">Syntax</span></span>

<span data-ttu-id="f9bc7-108">BITAND (\* \* *binarynumber1* \* \*, \* \* *binarynumber2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f9bc7-108">BITAND(\*\* *binarynumber1* \*\*, \*\* *binarynumber2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f9bc7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9bc7-109">Parameters</span></span>

|<span data-ttu-id="f9bc7-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f9bc7-110">**Name**</span></span>|<span data-ttu-id="f9bc7-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f9bc7-111">**Required/Optional**</span></span>|<span data-ttu-id="f9bc7-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f9bc7-112">**Data Type**</span></span>|<span data-ttu-id="f9bc7-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9bc7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f9bc7-114">_valeurs binaire1 binaires_</span><span class="sxs-lookup"><span data-stu-id="f9bc7-114">_binary number1_</span></span> <br/> |<span data-ttu-id="f9bc7-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f9bc7-115">Required</span></span>  <br/> |<span data-ttu-id="f9bc7-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="f9bc7-116">**Numeric**</span></span> <br/> |<span data-ttu-id="f9bc7-117">Premier nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="f9bc7-118">_binaire binaire2_</span><span class="sxs-lookup"><span data-stu-id="f9bc7-118">_binary number2_</span></span> <br/> |<span data-ttu-id="f9bc7-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f9bc7-119">Required</span></span>  <br/> |<span data-ttu-id="f9bc7-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="f9bc7-120">**Numeric**</span></span> <br/> |<span data-ttu-id="f9bc7-121">Deuxième nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9bc7-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9bc7-122">Remarks</span></span>

<span data-ttu-id="f9bc7-123">Vous pouvez utiliser cette fonction pour tester et modifier les propriétés d’une forme qui sont stockées sous forme de masque de bits, par exemple, le format de texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="f9bc7-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="f9bc7-124">Example</span></span>

<span data-ttu-id="f9bc7-125">BITAND (12, 6)</span><span class="sxs-lookup"><span data-stu-id="f9bc7-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="f9bc7-p103">Renvoie 4. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITAND(12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

