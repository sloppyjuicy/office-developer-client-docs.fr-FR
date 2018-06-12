---
title: UNICHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Renvoie le caractère Unicode à partir d’un nombre.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789973"
---
# <a name="unichar-function"></a><span data-ttu-id="239a8-103">UNICHAR, fonction</span><span class="sxs-lookup"><span data-stu-id="239a8-103">UNICHAR Function</span></span>

<span data-ttu-id="239a8-104">Renvoie le caractère Unicode à partir d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="239a8-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="239a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="239a8-105">Syntax</span></span>

<span data-ttu-id="239a8-106">UNICHAR (** *numéro* **)</span><span class="sxs-lookup"><span data-stu-id="239a8-106">UNICHAR (** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="239a8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="239a8-107">Parameters</span></span>

|<span data-ttu-id="239a8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="239a8-108">**Name**</span></span>|<span data-ttu-id="239a8-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="239a8-109">**Required/Optional**</span></span>|<span data-ttu-id="239a8-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="239a8-110">**Data Type**</span></span>|<span data-ttu-id="239a8-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="239a8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="239a8-112">_number_</span><span class="sxs-lookup"><span data-stu-id="239a8-112">_number_</span></span> <br/> |<span data-ttu-id="239a8-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="239a8-113">Required</span></span>  <br/> |<span data-ttu-id="239a8-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="239a8-114">**Integer**</span></span> <br/> |<span data-ttu-id="239a8-115">Entier compris entre 1 et 65 535 (inclus), ou la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="239a8-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="239a8-116">Note</span><span class="sxs-lookup"><span data-stu-id="239a8-116">Remarks</span></span>

<span data-ttu-id="239a8-117">La chaîne obtenue présente une longueur d’un caractère unicode (deux caractères).</span><span class="sxs-lookup"><span data-stu-id="239a8-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="239a8-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="239a8-118">Example</span></span>

<span data-ttu-id="239a8-119">UNICHAR (65)</span><span class="sxs-lookup"><span data-stu-id="239a8-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="239a8-120">Renvoie un (LETTRE MAJUSCULE LATINE A)</span><span class="sxs-lookup"><span data-stu-id="239a8-120">Returns A (Latin Capital Letter A)</span></span> 
  

