---
title: EVALTEXT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Évalue le texte dans le nom de la forme comme s’il s’agit d’une formule et renvoie le résultat.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438357"
---
# <a name="evaltext-function"></a><span data-ttu-id="a2c07-103">Fonction EVALTEXT</span><span class="sxs-lookup"><span data-stu-id="a2c07-103">EVALTEXT Function</span></span>

<span data-ttu-id="a2c07-104">Évalue le texte dans  _le nom de la forme_ comme s’il s’agit d’une formule et renvoie le résultat.</span><span class="sxs-lookup"><span data-stu-id="a2c07-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a2c07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2c07-105">Syntax</span></span>

<span data-ttu-id="a2c07-106">EVALTEXT(\*\* *shapename!theText* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a2c07-106">EVALTEXT(\*\* *shapename!theText* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a2c07-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2c07-107">Parameters</span></span>

|<span data-ttu-id="a2c07-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a2c07-108">**Name**</span></span>|<span data-ttu-id="a2c07-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a2c07-109">**Required/Optional**</span></span>|<span data-ttu-id="a2c07-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a2c07-110">**Data Type**</span></span>|<span data-ttu-id="a2c07-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2c07-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a2c07-112">_shapename!theText_</span><span class="sxs-lookup"><span data-stu-id="a2c07-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="a2c07-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2c07-113">Required</span></span>  <br/> |<span data-ttu-id="a2c07-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a2c07-114">**String**</span></span> <br/> |<span data-ttu-id="a2c07-115">Cellule générée lorsque la composition du texte de la forme associée est modifiée.</span><span class="sxs-lookup"><span data-stu-id="a2c07-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a2c07-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a2c07-116">Return value</span></span>

<span data-ttu-id="a2c07-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="a2c07-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2c07-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2c07-118">Remarks</span></span>

 <span data-ttu-id="a2c07-119">L’argument _shapename_ peut être utilisé pour faire référence au texte d’une forme autre que l’actuelle.</span><span class="sxs-lookup"><span data-stu-id="a2c07-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="a2c07-p101">En l’absence de texte, le résultat est zéro. Si le texte ne peut pas être calculé, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="a2c07-p101">If there is no text, the result is zero. If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="a2c07-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2c07-122">Example</span></span>

<span data-ttu-id="a2c07-123">EVALTEXT(Line.2!theText)</span><span class="sxs-lookup"><span data-stu-id="a2c07-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="a2c07-p102">Évalue le texte contenu dans la forme Trait.2. Si, par exemple, Trait.2 contient « 121,92 cm + 15,24 cm », la valeur 137,16 cm est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="a2c07-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

