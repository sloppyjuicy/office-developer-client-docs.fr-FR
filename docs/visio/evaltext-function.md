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
description: Évalue le texte dans l’argument shapename comme s’il a été une formule et renvoie le résultat.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788573"
---
# <a name="evaltext-function"></a><span data-ttu-id="27739-103">EVALTEXT, fonction</span><span class="sxs-lookup"><span data-stu-id="27739-103">EVALTEXT Function</span></span>

<span data-ttu-id="27739-104">Évalue le texte dans _l’argument shapename_ comme s’il a été une formule et renvoie le résultat.</span><span class="sxs-lookup"><span data-stu-id="27739-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="27739-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27739-105">Syntax</span></span>

<span data-ttu-id="27739-106">EVALTEXT (** *shapename ! theText* **)</span><span class="sxs-lookup"><span data-stu-id="27739-106">EVALTEXT(** *shapename!theText* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="27739-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27739-107">Parameters</span></span>

|<span data-ttu-id="27739-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="27739-108">**Name**</span></span>|<span data-ttu-id="27739-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="27739-109">**Required/Optional**</span></span>|<span data-ttu-id="27739-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="27739-110">**Data Type**</span></span>|<span data-ttu-id="27739-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="27739-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="27739-112">_l’argument shapename ! theText_</span><span class="sxs-lookup"><span data-stu-id="27739-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="27739-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="27739-113">Required</span></span>  <br/> |<span data-ttu-id="27739-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="27739-114">**String**</span></span> <br/> |<span data-ttu-id="27739-115">Cellule générée lorsque la composition du texte de la forme associée est modifiée.</span><span class="sxs-lookup"><span data-stu-id="27739-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="27739-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="27739-116">Return value</span></span>

<span data-ttu-id="27739-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="27739-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27739-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="27739-118">Remarks</span></span>

 <span data-ttu-id="27739-119">_l’argument shapename_ peut servir à faire référence au texte d’une forme autre que la forme active.</span><span class="sxs-lookup"><span data-stu-id="27739-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="27739-p101">En l’absence de texte, le résultat est zéro. Si le texte ne peut pas être calculé, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="27739-p101">If there is no text, the result is zero. If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="27739-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="27739-122">Example</span></span>

<span data-ttu-id="27739-123">EVALTEXT(Line.2!TheText)</span><span class="sxs-lookup"><span data-stu-id="27739-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="27739-p102">Évalue le texte contenu dans la forme Trait.2. Si, par exemple, Trait.2 contient « 121,92 cm + 15,24 cm », la valeur 137,16 cm est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="27739-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

