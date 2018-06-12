---
title: ARG, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Spécifie un argument que la cellule d’appel peut passer à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d’appel ne transmet une valeur pour l’argument. Renvoie la valeur spécifiée par la cellule d’appel et le paramètre argName correspondant.
ms.openlocfilehash: 3d0e126e0fa075ff2a07773197c1973e6b0249d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788051"
---
# <a name="arg-function"></a><span data-ttu-id="1027a-104">ARG, fonction</span><span class="sxs-lookup"><span data-stu-id="1027a-104">ARG Function</span></span>

<span data-ttu-id="1027a-105">Spécifie un argument que la cellule d’appel peut passer à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d’appel ne transmet une valeur pour l’argument.</span><span class="sxs-lookup"><span data-stu-id="1027a-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="1027a-106">Renvoie la valeur spécifiée par la cellule d’appel et le paramètre argName correspondant.</span><span class="sxs-lookup"><span data-stu-id="1027a-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1027a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1027a-107">Syntax</span></span>

<span data-ttu-id="1027a-108">ARG (** *argName* **, [** *defaultValue* **])</span><span class="sxs-lookup"><span data-stu-id="1027a-108">ARG(** *argName* **,[ ** *defaultValue* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1027a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1027a-109">Parameters</span></span>

|<span data-ttu-id="1027a-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="1027a-110">**Name**</span></span>|<span data-ttu-id="1027a-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="1027a-111">**Required/Optional**</span></span>|<span data-ttu-id="1027a-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="1027a-112">**Data Type**</span></span>|<span data-ttu-id="1027a-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="1027a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1027a-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="1027a-114">_argName_</span></span> <br/> |<span data-ttu-id="1027a-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1027a-115">Required</span></span>  <br/> |<span data-ttu-id="1027a-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="1027a-116">**String**</span></span> <br/> |<span data-ttu-id="1027a-117">Le nom d’un argument que peut transmettre la cellule d’appel à la fonction.</span><span class="sxs-lookup"><span data-stu-id="1027a-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="1027a-118">_Valeur par défaut_</span><span class="sxs-lookup"><span data-stu-id="1027a-118">_default Value_</span></span> <br/> |<span data-ttu-id="1027a-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="1027a-119">Optional</span></span>  <br/> |<span data-ttu-id="1027a-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="1027a-120">**Numeric**</span></span> <br/> |<span data-ttu-id="1027a-121">La valeur renvoyée par ARG si la cellule d’appel n’a pas transmis de valeur pour le paramètre _argName_ .</span><span class="sxs-lookup"><span data-stu-id="1027a-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1027a-122">Note</span><span class="sxs-lookup"><span data-stu-id="1027a-122">Remarks</span></span>

<span data-ttu-id="1027a-p103">Si vous développez des formes, vous pouvez créer des fonctions personnalisées en plaçant une expression dans une cellule et en appelant cette expression d’une ou plusieurs autres cellules. L’expression peut inclure des chaînes littérales, des fonctions ShapeSheet et des références de cellules. L’expression peut aussi inclure des arguments spécifiques transmis par la cellule d’appel.</span><span class="sxs-lookup"><span data-stu-id="1027a-p103">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells. The expression can include literal strings, ShapeSheet functions, and cell references. The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="1027a-126">La cellule d’appel spécifie la cellule qui contient la fonction personnalisée, ainsi que tous les arguments à transmettre à la fonction.</span><span class="sxs-lookup"><span data-stu-id="1027a-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="1027a-127">La cellule d’expression est évaluée et le résultat renvoyé à la cellule d’appel.</span><span class="sxs-lookup"><span data-stu-id="1027a-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="1027a-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="1027a-128">Example</span></span>

<span data-ttu-id="1027a-129">L’exemple suivant montre comment utiliser la fonction ARG conjointement avec la fonction EVALCELL pour trouver la valeur médiane parmi un ensemble de trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="1027a-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="1027a-130">Dans la cellule d’expression, placez le code suivant qui définit la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="1027a-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="1027a-131">Dans les cellules d’appel, placez le code suivant qui appelle la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="1027a-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


