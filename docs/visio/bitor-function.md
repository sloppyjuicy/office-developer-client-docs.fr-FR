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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit a la valeur 1 si le bit correspondant dans Numéro1 binaire ou binaire nombre2 est 1. Le bit est défini sur 0 uniquement si le bit correspondant est 0 en binaire Numéro1 et numéro2 binaire.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788111"
---
# <a name="bitor-function"></a><span data-ttu-id="252c2-104">BITOR, fonction</span><span class="sxs-lookup"><span data-stu-id="252c2-104">BITOR Function</span></span>

<span data-ttu-id="252c2-105">Renvoie un nombre binaire de 16 bits dans lequel chaque bit a la valeur 1 si le bit correspondant dans *Numéro1 binaire* ou *binaire nombre2* est 1.</span><span class="sxs-lookup"><span data-stu-id="252c2-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="252c2-106">Le bit est défini sur 0 uniquement si le bit correspondant est 0 en *binaire Numéro1* et *Numéro2 binaire* .</span><span class="sxs-lookup"><span data-stu-id="252c2-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="252c2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="252c2-107">Syntax</span></span>

<span data-ttu-id="252c2-108">BITOR (** *Numéro1 binaire* **, ** *Numéro2 binaire* **)</span><span class="sxs-lookup"><span data-stu-id="252c2-108">BITOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="252c2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="252c2-109">Parameters</span></span>

|<span data-ttu-id="252c2-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="252c2-110">**Name**</span></span>|<span data-ttu-id="252c2-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="252c2-111">**Required/Optional**</span></span>|<span data-ttu-id="252c2-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="252c2-112">**Data Type**</span></span>|<span data-ttu-id="252c2-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="252c2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="252c2-114">_nombre1 binaire_</span><span class="sxs-lookup"><span data-stu-id="252c2-114">_binary number1_</span></span> <br/> |<span data-ttu-id="252c2-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="252c2-115">Required</span></span>  <br/> |<span data-ttu-id="252c2-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="252c2-116">**Numeric**</span></span> <br/> |<span data-ttu-id="252c2-117">Premier nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="252c2-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="252c2-118">_nombre2 binaire_</span><span class="sxs-lookup"><span data-stu-id="252c2-118">_binary number2_</span></span> <br/> |<span data-ttu-id="252c2-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="252c2-119">Required</span></span>  <br/> |<span data-ttu-id="252c2-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="252c2-120">**Numeric**</span></span> <br/> |<span data-ttu-id="252c2-121">Deuxième nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="252c2-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="252c2-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="252c2-122">Return value</span></span>

<span data-ttu-id="252c2-123">Binaire de 16 bits</span><span class="sxs-lookup"><span data-stu-id="252c2-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="252c2-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="252c2-124">Example</span></span>

<span data-ttu-id="252c2-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="252c2-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="252c2-p103">Renvoie 14. Le 12 = 0...01100. Le 6 = 0...00110. Donc, BITOR(12,6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="252c2-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

