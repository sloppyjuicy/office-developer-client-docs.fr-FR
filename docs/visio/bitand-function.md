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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombrebinaire1 et nombrebinaire2 est 1. Sinon, le bit est défini sur 0.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788119"
---
# <a name="bitand-function"></a><span data-ttu-id="c9b84-104">BITAND, fonction</span><span class="sxs-lookup"><span data-stu-id="c9b84-104">BITAND Function</span></span>

<span data-ttu-id="c9b84-105">Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombrebinaire1 et nombrebinaire2 est 1.</span><span class="sxs-lookup"><span data-stu-id="c9b84-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="c9b84-106">Sinon, le bit est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="c9b84-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c9b84-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9b84-107">Syntax</span></span>

<span data-ttu-id="c9b84-108">BITAND (** *nombrebinaire1* **, ** *nombrebinaire2* **)</span><span class="sxs-lookup"><span data-stu-id="c9b84-108">BITAND(** *binarynumber1* **, ** *binarynumber2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c9b84-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9b84-109">Parameters</span></span>

|<span data-ttu-id="c9b84-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c9b84-110">**Name**</span></span>|<span data-ttu-id="c9b84-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c9b84-111">**Required/Optional**</span></span>|<span data-ttu-id="c9b84-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c9b84-112">**Data Type**</span></span>|<span data-ttu-id="c9b84-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="c9b84-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c9b84-114">_nombre1 binaire_</span><span class="sxs-lookup"><span data-stu-id="c9b84-114">_binary number1_</span></span> <br/> |<span data-ttu-id="c9b84-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c9b84-115">Required</span></span>  <br/> |<span data-ttu-id="c9b84-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="c9b84-116">**Numeric**</span></span> <br/> |<span data-ttu-id="c9b84-117">Premier nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c9b84-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="c9b84-118">_nombre2 binaire_</span><span class="sxs-lookup"><span data-stu-id="c9b84-118">_binary number2_</span></span> <br/> |<span data-ttu-id="c9b84-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c9b84-119">Required</span></span>  <br/> |<span data-ttu-id="c9b84-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="c9b84-120">**Numeric**</span></span> <br/> |<span data-ttu-id="c9b84-121">Deuxième nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c9b84-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9b84-122">Note</span><span class="sxs-lookup"><span data-stu-id="c9b84-122">Remarks</span></span>

<span data-ttu-id="c9b84-123">Vous pouvez utiliser cette fonction pour tester et modifier les propriétés d’une forme qui sont stockées sous forme de masque de bits, par exemple, le format de texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="c9b84-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="c9b84-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9b84-124">Example</span></span>

<span data-ttu-id="c9b84-125">BITAND(12,6)</span><span class="sxs-lookup"><span data-stu-id="c9b84-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="c9b84-p103">Renvoie 4. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITAND(12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="c9b84-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

