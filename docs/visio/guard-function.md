---
title: GUARD, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protège l’expression contre la suppression ou la modification par les actions effectuées dans la fenêtre de dessin, par exemple, que le déplacement, le redimensionnement, le regroupement ou la dissociation des formes.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788739"
---
# <a name="guard-function"></a><span data-ttu-id="be936-103">GUARD, fonction</span><span class="sxs-lookup"><span data-stu-id="be936-103">GUARD Function</span></span>

<span data-ttu-id="be936-104">Protège *l’expression* contre la suppression ou la modification par les actions effectuées dans la fenêtre de dessin, par exemple, que le déplacement, le redimensionnement, le regroupement ou la dissociation des formes.</span><span class="sxs-lookup"><span data-stu-id="be936-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="be936-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be936-105">Syntax</span></span>

<span data-ttu-id="be936-106">GUARD (** *expression* **)</span><span class="sxs-lookup"><span data-stu-id="be936-106">GUARD(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="be936-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be936-107">Parameters</span></span>

|<span data-ttu-id="be936-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="be936-108">**Name**</span></span>|<span data-ttu-id="be936-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="be936-109">**Required/Optional**</span></span>|<span data-ttu-id="be936-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="be936-110">**Data Type**</span></span>|<span data-ttu-id="be936-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="be936-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="be936-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="be936-112">_expression_</span></span> <br/> |<span data-ttu-id="be936-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="be936-113">Required</span></span>  <br/> |<span data-ttu-id="be936-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="be936-114">**String**</span></span> <br/> |<span data-ttu-id="be936-115">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.</span><span class="sxs-lookup"><span data-stu-id="be936-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be936-116">Note</span><span class="sxs-lookup"><span data-stu-id="be936-116">Remarks</span></span>

<span data-ttu-id="be936-117">Les cellules les plus souvent concernées par la fonction GUARD sont les cellules Width, Height, PinX et PinY.</span><span class="sxs-lookup"><span data-stu-id="be936-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="be936-p101">La protection d’une formule dans n’importe quelle cellule empêche que la valeur de cette dernière ne soit modifiée par des actions exécutées dans la fenêtre de dessin. Une même action peut toutefois avoir une incidence sur plusieurs cellules et chacune d’elles doit être protégée pour éviter des modifications inattendues de l’aspect des formes.</span><span class="sxs-lookup"><span data-stu-id="be936-p101">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window. However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="be936-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="be936-120">Example</span></span>

<span data-ttu-id="be936-121">GUARD(TEXTWIDTH(TheText) + 0,5 po)</span><span class="sxs-lookup"><span data-stu-id="be936-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="be936-p102">Cette expression dans la cellule Largeur de la section Transformation de la forme évite que l’expression (TEXTWIDTH(TheText) + 0,5 po) ne soit remplacée par une autre valeur lorsque la largeur de la forme est modifiée dans la fenêtre de dessin. La cellule TheText est générée lorsque la composition du texte de la forme qui y est associée est modifiée.</span><span class="sxs-lookup"><span data-stu-id="be936-p102">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window. TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

