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
description: Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies. Si l'une des expressions logiques est FALSe ou 0, la fonction et renvoie la valeur FALSe (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341558"
---
# <a name="and-function"></a><span data-ttu-id="29211-104">Fonction AND</span><span class="sxs-lookup"><span data-stu-id="29211-104">AND Function</span></span>

<span data-ttu-id="29211-105">Renvoie la valeur TRUE (1) si toutes les expressions logiques fournies sont vraies.</span><span class="sxs-lookup"><span data-stu-id="29211-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="29211-106">Si l'une des expressions logiques est FALSe ou 0, la fonction et renvoie la valeur FALSe (0).</span><span class="sxs-lookup"><span data-stu-id="29211-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="29211-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29211-107">Syntax</span></span>

<span data-ttu-id="29211-108">et (\* \* *opérateur logique expression1* \* \*, \* \* caractères *logiques expression2* \* \*,..., \* \* *logical expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="29211-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="29211-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29211-109">Parameters</span></span>

|<span data-ttu-id="29211-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="29211-110">**Name**</span></span>|<span data-ttu-id="29211-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="29211-111">**Required/Optional**</span></span>|<span data-ttu-id="29211-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="29211-112">**Data Type**</span></span>|<span data-ttu-id="29211-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="29211-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="29211-114">_expression logique_</span><span class="sxs-lookup"><span data-stu-id="29211-114">_logical expression_</span></span> <br/> |<span data-ttu-id="29211-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="29211-115">Required</span></span>  <br/> |<span data-ttu-id="29211-116">**String**</span><span class="sxs-lookup"><span data-stu-id="29211-116">**String**</span></span> <br/> | <span data-ttu-id="29211-p103">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. Toute expression donnant une valeur différente de zéro est considérée comme vraie (valeur TRUE).</span><span class="sxs-lookup"><span data-stu-id="29211-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="29211-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="29211-119">Example</span></span>

<span data-ttu-id="29211-120">ET (hauteur \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="29211-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="29211-121">Renvoie TRUE si les deux expressions sont vraies.</span><span class="sxs-lookup"><span data-stu-id="29211-121">Returns TRUE if both expressions are TRUE.</span></span> <span data-ttu-id="29211-122">Renvoie FALSE si l’une des expressions est fausse.</span><span class="sxs-lookup"><span data-stu-id="29211-122">Returns FALSE if either expression is FALSE.</span></span>
  

