---
title: BITOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans le nombre binaire numéro1 ou le nombre binaire2 est 1. Le bit est définie sur 0 uniquement si le bit correspondant est 0 dans le nombre binaire 1 et le nombre binaire 2 .
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408081"
---
# <a name="bitor-function"></a><span data-ttu-id="3dfde-104">Fonction BITOR</span><span class="sxs-lookup"><span data-stu-id="3dfde-104">BITOR Function</span></span>

<span data-ttu-id="3dfde-105">Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 si le bit correspondant dans le nombre  *binaire numéro1*  ou le nombre  *binaire2*  est 1.</span><span class="sxs-lookup"><span data-stu-id="3dfde-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="3dfde-106">Le bit est définie sur 0 uniquement si le bit correspondant est 0 dans le  *nombre binaire 1*  et  *le nombre binaire 2*  .</span><span class="sxs-lookup"><span data-stu-id="3dfde-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3dfde-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dfde-107">Syntax</span></span>

<span data-ttu-id="3dfde-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="3dfde-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3dfde-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dfde-109">Parameters</span></span>

|<span data-ttu-id="3dfde-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3dfde-110">**Name**</span></span>|<span data-ttu-id="3dfde-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3dfde-111">**Required/Optional**</span></span>|<span data-ttu-id="3dfde-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3dfde-112">**Data Type**</span></span>|<span data-ttu-id="3dfde-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="3dfde-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3dfde-114">_binary number1_</span><span class="sxs-lookup"><span data-stu-id="3dfde-114">_binary number1_</span></span> <br/> |<span data-ttu-id="3dfde-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3dfde-115">Required</span></span>  <br/> |<span data-ttu-id="3dfde-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="3dfde-116">**Numeric**</span></span> <br/> |<span data-ttu-id="3dfde-117">Premier nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3dfde-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="3dfde-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="3dfde-118">_binary number2_</span></span> <br/> |<span data-ttu-id="3dfde-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3dfde-119">Required</span></span>  <br/> |<span data-ttu-id="3dfde-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="3dfde-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3dfde-121">Deuxième nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3dfde-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3dfde-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3dfde-122">Return value</span></span>

<span data-ttu-id="3dfde-123">Binaire de 16 bits</span><span class="sxs-lookup"><span data-stu-id="3dfde-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="3dfde-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="3dfde-124">Example</span></span>

<span data-ttu-id="3dfde-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="3dfde-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="3dfde-p103">Renvoie 14. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITOR(12,6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="3dfde-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

