---
title: BITXOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans l’un ou l’autre, mais pas dans le nombre binaire number1 et le nombre binaire 2, est 1. Dans le cas contraire, le bit est définie sur 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439232"
---
# <a name="bitxor-function"></a><span data-ttu-id="7ed84-104">Fonction BITXOR</span><span class="sxs-lookup"><span data-stu-id="7ed84-104">BITXOR Function</span></span>

<span data-ttu-id="7ed84-105">Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans l’un ou l’autre, mais pas dans le nombre binaire number1 et le nombre binaire 2, est 1.</span><span class="sxs-lookup"><span data-stu-id="7ed84-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="7ed84-106">Dans le cas contraire, le bit est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="7ed84-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7ed84-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ed84-107">Syntax</span></span>

<span data-ttu-id="7ed84-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="7ed84-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7ed84-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ed84-109">Parameters</span></span>

|<span data-ttu-id="7ed84-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7ed84-110">**Name**</span></span>|<span data-ttu-id="7ed84-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7ed84-111">**Required/Optional**</span></span>|<span data-ttu-id="7ed84-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7ed84-112">**Data Type**</span></span>|<span data-ttu-id="7ed84-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="7ed84-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7ed84-114">_binary number1_</span><span class="sxs-lookup"><span data-stu-id="7ed84-114">_binary number1_</span></span> <br/> |<span data-ttu-id="7ed84-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ed84-115">Required</span></span>  <br/> |<span data-ttu-id="7ed84-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="7ed84-116">**Numeric**</span></span> <br/> |<span data-ttu-id="7ed84-117">Premier nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7ed84-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="7ed84-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="7ed84-118">_binary number2_</span></span> <br/> |<span data-ttu-id="7ed84-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ed84-119">Required</span></span>  <br/> |<span data-ttu-id="7ed84-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="7ed84-120">**Numeric**</span></span> <br/> |<span data-ttu-id="7ed84-121">Deuxième nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7ed84-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7ed84-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7ed84-122">Return value</span></span>

<span data-ttu-id="7ed84-123">Binaire de 16 bits</span><span class="sxs-lookup"><span data-stu-id="7ed84-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="7ed84-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="7ed84-124">Example</span></span>

<span data-ttu-id="7ed84-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="7ed84-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="7ed84-p103">Renvoie 10. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITXOR(12,6) = 0...01010.</span><span class="sxs-lookup"><span data-stu-id="7ed84-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

