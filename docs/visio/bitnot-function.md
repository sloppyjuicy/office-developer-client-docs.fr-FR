---
title: BITNOT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombre binaire est égal à 0. Sinon, le bit est défini sur 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788094"
---
# <a name="bitnot-function"></a><span data-ttu-id="86cb8-104">BITNOT, fonction</span><span class="sxs-lookup"><span data-stu-id="86cb8-104">BITNOT Function</span></span>

<span data-ttu-id="86cb8-105">Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant dans nombre binaire est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="86cb8-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="86cb8-106">Sinon, le bit est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="86cb8-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="86cb8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86cb8-107">Syntax</span></span>

<span data-ttu-id="86cb8-108">BITNOT (** *nombre binaire* **)</span><span class="sxs-lookup"><span data-stu-id="86cb8-108">BITNOT(** *binary number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="86cb8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86cb8-109">Parameters</span></span>

|<span data-ttu-id="86cb8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="86cb8-110">**Name**</span></span>|<span data-ttu-id="86cb8-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="86cb8-111">**Required/Optional**</span></span>|<span data-ttu-id="86cb8-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="86cb8-112">**Data Type**</span></span>|<span data-ttu-id="86cb8-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="86cb8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="86cb8-114">_nombre binaire_</span><span class="sxs-lookup"><span data-stu-id="86cb8-114">_binary number_</span></span> <br/> |<span data-ttu-id="86cb8-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="86cb8-115">Required</span></span>  <br/> |<span data-ttu-id="86cb8-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="86cb8-116">**Numeric**</span></span> <br/> |<span data-ttu-id="86cb8-117">Nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="86cb8-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="86cb8-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="86cb8-118">Return value</span></span>

<span data-ttu-id="86cb8-119">Binaire de 16 bits</span><span class="sxs-lookup"><span data-stu-id="86cb8-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="86cb8-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="86cb8-120">Example</span></span>

<span data-ttu-id="86cb8-121">BITNOT(6)</span><span class="sxs-lookup"><span data-stu-id="86cb8-121">BITNOT(6)</span></span>
  
<span data-ttu-id="86cb8-p103">Renvoie 65529. Le 6 = 0...00110. Donc, BITNOT(6) = 1...11001.</span><span class="sxs-lookup"><span data-stu-id="86cb8-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

