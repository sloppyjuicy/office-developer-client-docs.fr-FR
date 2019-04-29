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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit prend la valeur 1 si le bit correspondant dans l'un ou l'autre des nombres binaire1 et binaire2 est 1. Dans le cas contraire, le bit prend la valeur 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439232"
---
# <a name="bitxor-function"></a><span data-ttu-id="3603c-104">Fonction BITXOR</span><span class="sxs-lookup"><span data-stu-id="3603c-104">BITXOR Function</span></span>

<span data-ttu-id="3603c-105">Renvoie un nombre binaire de 16 bits dans lequel chaque bit prend la valeur 1 si le bit correspondant dans l'un ou l'autre des nombres binaire1 et binaire2 est 1.</span><span class="sxs-lookup"><span data-stu-id="3603c-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="3603c-106">Dans le cas contraire, le bit prend la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="3603c-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3603c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3603c-107">Syntax</span></span>

<span data-ttu-id="3603c-108">BITXOR (\* \* \* \* *binaire nombre1* \* \*, \* \* *binaires binaire2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3603c-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3603c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3603c-109">Parameters</span></span>

|<span data-ttu-id="3603c-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3603c-110">**Name**</span></span>|<span data-ttu-id="3603c-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3603c-111">**Required/Optional**</span></span>|<span data-ttu-id="3603c-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3603c-112">**Data Type**</span></span>|<span data-ttu-id="3603c-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="3603c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3603c-114">_valeurs binaire1 binaires_</span><span class="sxs-lookup"><span data-stu-id="3603c-114">_binary number1_</span></span> <br/> |<span data-ttu-id="3603c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3603c-115">Required</span></span>  <br/> |<span data-ttu-id="3603c-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="3603c-116">**Numeric**</span></span> <br/> |<span data-ttu-id="3603c-117">Premier nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3603c-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="3603c-118">_binaire binaire2_</span><span class="sxs-lookup"><span data-stu-id="3603c-118">_binary number2_</span></span> <br/> |<span data-ttu-id="3603c-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3603c-119">Required</span></span>  <br/> |<span data-ttu-id="3603c-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="3603c-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3603c-121">Deuxième nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3603c-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3603c-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3603c-122">Return value</span></span>

<span data-ttu-id="3603c-123">Binaire de 16 bits</span><span class="sxs-lookup"><span data-stu-id="3603c-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="3603c-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="3603c-124">Example</span></span>

<span data-ttu-id="3603c-125">BITXOR (12, 6)</span><span class="sxs-lookup"><span data-stu-id="3603c-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="3603c-p103">Renvoie 10. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITXOR(12,6) = 0...01010.</span><span class="sxs-lookup"><span data-stu-id="3603c-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

