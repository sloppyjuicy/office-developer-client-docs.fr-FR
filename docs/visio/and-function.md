---
title: AND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies. Si une des expressions logiques est FALSE ou 0, la fonction et renvoie la valeur FALSE (0).
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788032"
---
# <a name="and-function"></a><span data-ttu-id="9f4e4-104">AND, fonction</span><span class="sxs-lookup"><span data-stu-id="9f4e4-104">AND Function</span></span>

<span data-ttu-id="9f4e4-105">Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies.</span><span class="sxs-lookup"><span data-stu-id="9f4e4-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="9f4e4-106">Si une des expressions logiques est FALSE ou 0, la fonction et renvoie la valeur FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="9f4e4-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9f4e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f4e4-107">Syntax</span></span>

<span data-ttu-id="9f4e4-108">ET (** *expression1 logique* **, ** *expression2 logique* **,..., ** *expressionN logique* **)</span><span class="sxs-lookup"><span data-stu-id="9f4e4-108">AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f4e4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f4e4-109">Parameters</span></span>

|<span data-ttu-id="9f4e4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f4e4-110">**Name**</span></span>|<span data-ttu-id="9f4e4-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9f4e4-111">**Required/Optional**</span></span>|<span data-ttu-id="9f4e4-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9f4e4-112">**Data Type**</span></span>|<span data-ttu-id="9f4e4-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="9f4e4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f4e4-114">_expression logique_</span><span class="sxs-lookup"><span data-stu-id="9f4e4-114">_logical expression_</span></span> <br/> |<span data-ttu-id="9f4e4-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9f4e4-115">Required</span></span>  <br/> |<span data-ttu-id="9f4e4-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f4e4-116">**String**</span></span> <br/> | <span data-ttu-id="9f4e4-p103">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. Toute expression donnant une valeur différente de zéro est considérée comme vraie (valeur TRUE).</span><span class="sxs-lookup"><span data-stu-id="9f4e4-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="9f4e4-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="9f4e4-119">Example</span></span>

<span data-ttu-id="9f4e4-120">ET (hauteur \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="9f4e4-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="9f4e4-p104">Renvoie TRUE si les deux expressions sont vraies. Renvoie FALSE si l’une des expressions est fausse.</span><span class="sxs-lookup"><span data-stu-id="9f4e4-p104">Returns TRUE if both expressions are TRUE. Returns FALSE if either expression is FALSE.</span></span>
  

