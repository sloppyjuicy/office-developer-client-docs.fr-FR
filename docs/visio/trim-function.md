---
title: TRIM, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Supprime tout espace du texte, à l’exception des espaces entre les mots.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789942"
---
# <a name="trim-function"></a><span data-ttu-id="dac7e-103">TRIM, fonction</span><span class="sxs-lookup"><span data-stu-id="dac7e-103">TRIM Function</span></span>

<span data-ttu-id="dac7e-104">Supprime tout espace du texte, à l’exception des espaces entre les mots.</span><span class="sxs-lookup"><span data-stu-id="dac7e-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dac7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac7e-105">Syntax</span></span>

<span data-ttu-id="dac7e-106">TRIM (** *texte* **)</span><span class="sxs-lookup"><span data-stu-id="dac7e-106">TRIM (** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dac7e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac7e-107">Parameters</span></span>

|<span data-ttu-id="dac7e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="dac7e-108">**Name**</span></span>|<span data-ttu-id="dac7e-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="dac7e-109">**Required/Optional**</span></span>|<span data-ttu-id="dac7e-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="dac7e-110">**Data Type**</span></span>|<span data-ttu-id="dac7e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="dac7e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dac7e-112">_text_</span><span class="sxs-lookup"><span data-stu-id="dac7e-112">_text_</span></span> <br/> |<span data-ttu-id="dac7e-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dac7e-113">Required</span></span>  <br/> |<span data-ttu-id="dac7e-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="dac7e-114">**String**</span></span> <br/> |<span data-ttu-id="dac7e-115">Texte dont vous souhaitez supprimer les espaces.</span><span class="sxs-lookup"><span data-stu-id="dac7e-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dac7e-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="dac7e-116">Return value</span></span>

<span data-ttu-id="dac7e-117">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dac7e-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dac7e-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="dac7e-118">Remarks</span></span>

<span data-ttu-id="dac7e-119">Vous pouvez utiliser la fonction TRIM sur du texte provenant d’une autre application qui utilise un espacement irrégulier.</span><span class="sxs-lookup"><span data-stu-id="dac7e-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="dac7e-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="dac7e-120">Example</span></span>

<span data-ttu-id="dac7e-121">TRIM (« janvier 1, 2003 »)</span><span class="sxs-lookup"><span data-stu-id="dac7e-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="dac7e-122">Renvoie "2 janvier 2003".</span><span class="sxs-lookup"><span data-stu-id="dac7e-122">Returns "January 1, 2003".</span></span> 
  

