---
title: CHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Renvoie le caractère ANSI pour un nombre.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788233"
---
# <a name="char-function"></a><span data-ttu-id="687ee-103">CHAR, fonction</span><span class="sxs-lookup"><span data-stu-id="687ee-103">CHAR Function</span></span>

<span data-ttu-id="687ee-104">Renvoie le caractère ANSI pour un nombre.</span><span class="sxs-lookup"><span data-stu-id="687ee-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="687ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="687ee-105">Syntax</span></span>

<span data-ttu-id="687ee-106">CHAR (** *numéro* **)</span><span class="sxs-lookup"><span data-stu-id="687ee-106">CHAR(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="687ee-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="687ee-107">Parameters</span></span>

|<span data-ttu-id="687ee-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="687ee-108">**Name**</span></span>|<span data-ttu-id="687ee-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="687ee-109">**Required/Optional**</span></span>|<span data-ttu-id="687ee-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="687ee-110">**Data Type**</span></span>|<span data-ttu-id="687ee-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="687ee-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="687ee-112">_number_</span><span class="sxs-lookup"><span data-stu-id="687ee-112">_number_</span></span> <br/> |<span data-ttu-id="687ee-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="687ee-113">Required</span></span>  <br/> |<span data-ttu-id="687ee-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="687ee-114">**Number**</span></span> <br/> |<span data-ttu-id="687ee-115">Nombre dont vous souhaitez obtenir le caractère ANSI.</span><span class="sxs-lookup"><span data-stu-id="687ee-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="687ee-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="687ee-116">Remarks</span></span>

<span data-ttu-id="687ee-117">La chaîne obtenue est un caractère.</span><span class="sxs-lookup"><span data-stu-id="687ee-117">The resulting string is one character in length.</span></span> <span data-ttu-id="687ee-118">Le paramètre _nombre_ doit être un entier compris entre 1 et 255 (inclus), ou la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="687ee-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="687ee-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="687ee-119">Example</span></span>

<span data-ttu-id="687ee-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="687ee-120">CHAR(9)</span></span> 
  
<span data-ttu-id="687ee-121">Renvoie le caractère de tabulation.</span><span class="sxs-lookup"><span data-stu-id="687ee-121">Returns the tab character.</span></span> 
  

