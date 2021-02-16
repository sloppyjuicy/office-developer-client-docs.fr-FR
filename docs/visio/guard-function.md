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
description: Protège l’expression contre la suppression et le changement par des actions effectuées dans la fenêtre de dessin, telles que le déplacement, le resserrage, le regroupement ou la suppression de formes.
ms.openlocfilehash: 0bdfa023d53e739a970cab65b1dbd67bc1a44461
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408151"
---
# <a name="guard-function"></a><span data-ttu-id="ffdcf-103">Fonction GUARD</span><span class="sxs-lookup"><span data-stu-id="ffdcf-103">GUARD Function</span></span>

<span data-ttu-id="ffdcf-104">Protège  *l’expression*  contre la suppression et le changement par des actions effectuées dans la fenêtre de dessin, telles que le déplacement, le resserrage, le regroupement ou la suppression de formes.</span><span class="sxs-lookup"><span data-stu-id="ffdcf-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ffdcf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffdcf-105">Syntax</span></span>

<span data-ttu-id="ffdcf-106">GUARD(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ffdcf-106">GUARD(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ffdcf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffdcf-107">Parameters</span></span>

|<span data-ttu-id="ffdcf-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ffdcf-108">**Name**</span></span>|<span data-ttu-id="ffdcf-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ffdcf-109">**Required/Optional**</span></span>|<span data-ttu-id="ffdcf-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ffdcf-110">**Data Type**</span></span>|<span data-ttu-id="ffdcf-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ffdcf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ffdcf-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ffdcf-112">_expression_</span></span> <br/> |<span data-ttu-id="ffdcf-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ffdcf-113">Required</span></span>  <br/> |<span data-ttu-id="ffdcf-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ffdcf-114">**String**</span></span> <br/> |<span data-ttu-id="ffdcf-115">Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.</span><span class="sxs-lookup"><span data-stu-id="ffdcf-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffdcf-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffdcf-116">Remarks</span></span>

<span data-ttu-id="ffdcf-117">Les cellules les plus souvent concernées par la fonction GUARD sont les cellules Width, Height, PinX et PinY.</span><span class="sxs-lookup"><span data-stu-id="ffdcf-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="ffdcf-p101">La protection d’une formule dans n’importe quelle cellule empêche que la valeur de cette dernière ne soit modifiée par des actions exécutées dans la fenêtre de dessin. Une même action peut toutefois avoir une incidence sur plusieurs cellules et chacune d’elles doit être protégée pour éviter des modifications inattendues de l’aspect des formes.</span><span class="sxs-lookup"><span data-stu-id="ffdcf-p101">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window. However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ffdcf-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="ffdcf-120">Example</span></span>

<span data-ttu-id="ffdcf-121">GUARD(TEXTWIDTH(TheText) + 0,5 po)</span><span class="sxs-lookup"><span data-stu-id="ffdcf-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="ffdcf-p102">Cette expression dans la cellule Largeur de la section Transformation de la forme évite que l’expression (TEXTWIDTH(TheText) + 0,5 po) ne soit remplacée par une autre valeur lorsque la largeur de la forme est modifiée dans la fenêtre de dessin. La cellule TheText est générée lorsque la composition du texte de la forme qui y est associée est modifiée.</span><span class="sxs-lookup"><span data-stu-id="ffdcf-p102">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window. TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

