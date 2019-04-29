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
description: Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant en nombre binaire est égal à 0. Dans le cas contraire, le bit prend la valeur 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438833"
---
# <a name="bitnot-function"></a><span data-ttu-id="06f54-104">Fonction BITNOT</span><span class="sxs-lookup"><span data-stu-id="06f54-104">BITNOT Function</span></span>

<span data-ttu-id="06f54-105">Renvoie un nombre binaire de 16 bits dans lequel chaque bit est défini sur 1 uniquement si le bit correspondant en nombre binaire est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="06f54-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="06f54-106">Dans le cas contraire, le bit prend la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="06f54-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="06f54-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06f54-107">Syntax</span></span>

<span data-ttu-id="06f54-108">BITNOT (\* \* *nombre binaire* \* \*)</span><span class="sxs-lookup"><span data-stu-id="06f54-108">BITNOT(\*\* *binary number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="06f54-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06f54-109">Parameters</span></span>

|<span data-ttu-id="06f54-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="06f54-110">**Name**</span></span>|<span data-ttu-id="06f54-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="06f54-111">**Required/Optional**</span></span>|<span data-ttu-id="06f54-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="06f54-112">**Data Type**</span></span>|<span data-ttu-id="06f54-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="06f54-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="06f54-114">_nombre binaire_</span><span class="sxs-lookup"><span data-stu-id="06f54-114">_binary number_</span></span> <br/> |<span data-ttu-id="06f54-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="06f54-115">Required</span></span>  <br/> |<span data-ttu-id="06f54-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="06f54-116">**Numeric**</span></span> <br/> |<span data-ttu-id="06f54-117">Nombre binaire de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="06f54-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="06f54-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06f54-118">Return value</span></span>

<span data-ttu-id="06f54-119">Binaire de 16 bits</span><span class="sxs-lookup"><span data-stu-id="06f54-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="06f54-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="06f54-120">Example</span></span>

<span data-ttu-id="06f54-121">BITNOT (6)</span><span class="sxs-lookup"><span data-stu-id="06f54-121">BITNOT(6)</span></span>
  
<span data-ttu-id="06f54-p103">Renvoie 65529. Le 6 = 0...00110. Donc, BITNOT(6) = 1...11001.</span><span class="sxs-lookup"><span data-stu-id="06f54-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

