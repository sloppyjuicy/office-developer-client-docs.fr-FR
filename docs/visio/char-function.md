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
description: Renvoie le caractère ANSI d'un nombre.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341908"
---
# <a name="char-function"></a><span data-ttu-id="93f06-103">Fonction CHAR</span><span class="sxs-lookup"><span data-stu-id="93f06-103">CHAR Function</span></span>

<span data-ttu-id="93f06-104">Renvoie le caractère ANSI d'un nombre.</span><span class="sxs-lookup"><span data-stu-id="93f06-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="93f06-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93f06-105">Syntax</span></span>

<span data-ttu-id="93f06-106">CHAR (\* \* *nombre* \* \*)</span><span class="sxs-lookup"><span data-stu-id="93f06-106">CHAR(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="93f06-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93f06-107">Parameters</span></span>

|<span data-ttu-id="93f06-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="93f06-108">**Name**</span></span>|<span data-ttu-id="93f06-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="93f06-109">**Required/Optional**</span></span>|<span data-ttu-id="93f06-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="93f06-110">**Data Type**</span></span>|<span data-ttu-id="93f06-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="93f06-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="93f06-112">_number_</span><span class="sxs-lookup"><span data-stu-id="93f06-112">_number_</span></span> <br/> |<span data-ttu-id="93f06-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="93f06-113">Required</span></span>  <br/> |<span data-ttu-id="93f06-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="93f06-114">**Number**</span></span> <br/> |<span data-ttu-id="93f06-115">Nombre dont vous souhaitez obtenir le caractère ANSI.</span><span class="sxs-lookup"><span data-stu-id="93f06-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93f06-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="93f06-116">Remarks</span></span>

<span data-ttu-id="93f06-117">La chaîne renvoyée comporte un seul caractère.</span><span class="sxs-lookup"><span data-stu-id="93f06-117">The resulting string is one character in length.</span></span> <span data-ttu-id="93f06-118">Le paramètre _Number_ doit être un entier compris entre 1 et 255 (inclus), sinon la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="93f06-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="93f06-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="93f06-119">Example</span></span>

<span data-ttu-id="93f06-120">CHAR (9)</span><span class="sxs-lookup"><span data-stu-id="93f06-120">CHAR(9)</span></span> 
  
<span data-ttu-id="93f06-121">Renvoie le caractère de tabulation.</span><span class="sxs-lookup"><span data-stu-id="93f06-121">Returns the tab character.</span></span> 
  

