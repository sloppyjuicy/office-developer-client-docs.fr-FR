---
title: ARG, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Spécifie un argument que la cellule d'appel peut transmettre à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d'appel ne transmet pas de valeur pour l'argument. Renvoie la valeur spécifiée par la cellule Calling et le paramètre argName correspondant.
ms.openlocfilehash: f85c3dc4a49878b034674330f272a63e79c17d49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341432"
---
# <a name="arg-function"></a><span data-ttu-id="0713c-104">Fonction ARG</span><span class="sxs-lookup"><span data-stu-id="0713c-104">ARG Function</span></span>

<span data-ttu-id="0713c-105">Spécifie un argument que la cellule d'appel peut transmettre à une fonction personnalisée, ainsi que la valeur par défaut renvoyée par la fonction personnalisée si la cellule d'appel ne transmet pas de valeur pour l'argument.</span><span class="sxs-lookup"><span data-stu-id="0713c-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="0713c-106">Renvoie la valeur spécifiée par la cellule Calling et le paramètre argName correspondant.</span><span class="sxs-lookup"><span data-stu-id="0713c-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0713c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0713c-107">Syntax</span></span>

<span data-ttu-id="0713c-108">ARG (\* \* *argName* \* *, [* \* *DefaultValue* \* \*])</span><span class="sxs-lookup"><span data-stu-id="0713c-108">ARG(\*\* *argName* \*\*,[ \*\* *defaultValue* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0713c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0713c-109">Parameters</span></span>

|<span data-ttu-id="0713c-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0713c-110">**Name**</span></span>|<span data-ttu-id="0713c-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="0713c-111">**Required/Optional**</span></span>|<span data-ttu-id="0713c-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="0713c-112">**Data Type**</span></span>|<span data-ttu-id="0713c-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="0713c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0713c-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="0713c-114">_argName_</span></span> <br/> |<span data-ttu-id="0713c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0713c-115">Required</span></span>  <br/> |<span data-ttu-id="0713c-116">**String**</span><span class="sxs-lookup"><span data-stu-id="0713c-116">**String**</span></span> <br/> |<span data-ttu-id="0713c-117">Le nom d’un argument que peut transmettre la cellule d’appel à la fonction.</span><span class="sxs-lookup"><span data-stu-id="0713c-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="0713c-118">_Valeur par défaut_</span><span class="sxs-lookup"><span data-stu-id="0713c-118">_default Value_</span></span> <br/> |<span data-ttu-id="0713c-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="0713c-119">Optional</span></span>  <br/> |<span data-ttu-id="0713c-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="0713c-120">**Numeric**</span></span> <br/> |<span data-ttu-id="0713c-121">Valeur renvoyée par ARG si la cellule d'appel n'a pas transmis de valeur pour le paramètre _argName_ .</span><span class="sxs-lookup"><span data-stu-id="0713c-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0713c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="0713c-122">Remarks</span></span>

<span data-ttu-id="0713c-p103">Si vous développez des formes, vous pouvez créer des fonctions personnalisées en plaçant une expression dans une cellule et en appelant cette expression d’une ou plusieurs autres cellules. L’expression peut inclure des chaînes littérales, des fonctions ShapeSheet et des références de cellules. L’expression peut aussi inclure des arguments spécifiques transmis par la cellule d’appel.</span><span class="sxs-lookup"><span data-stu-id="0713c-p103">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells. The expression can include literal strings, ShapeSheet functions, and cell references. The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="0713c-126">La cellule d’appel spécifie la cellule contenant la fonction personnalisée ainsi que les arguments qu’elle a besoin de transmettre à la fonction.</span><span class="sxs-lookup"><span data-stu-id="0713c-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="0713c-127">La cellule d’expression est évaluée et le résultat renvoyé à la cellule d’appel.</span><span class="sxs-lookup"><span data-stu-id="0713c-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="0713c-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="0713c-128">Example</span></span>

<span data-ttu-id="0713c-129">L’exemple suivant montre comment utiliser la fonction ARG conjointement avec la fonction EVALCELL pour trouver la valeur médiane parmi un ensemble de trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="0713c-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="0713c-130">Dans la cellule d’expression, placez le code suivant qui définit la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="0713c-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="0713c-131">Dans les cellules d’appel, placez le code suivant qui appelle la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="0713c-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


