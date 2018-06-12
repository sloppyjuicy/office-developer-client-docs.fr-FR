---
title: PAGENAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Renvoie le nom de la page sous forme de chaîne.
ms.openlocfilehash: 530707530d60955f460d6a747024b98ebdd5ab62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789213"
---
# <a name="pagename-function"></a><span data-ttu-id="fa55f-103">PAGENAME, fonction</span><span class="sxs-lookup"><span data-stu-id="fa55f-103">PAGENAME Function</span></span>

<span data-ttu-id="fa55f-104">Renvoie le nom de la page sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="fa55f-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fa55f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa55f-105">Syntax</span></span>

<span data-ttu-id="fa55f-106">PAGENAME (** *Idlang_opt* **)</span><span class="sxs-lookup"><span data-stu-id="fa55f-106">PAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fa55f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa55f-107">Parameters</span></span>

|<span data-ttu-id="fa55f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fa55f-108">**Name**</span></span>|<span data-ttu-id="fa55f-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="fa55f-109">**Required/Optional**</span></span>|<span data-ttu-id="fa55f-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="fa55f-110">**Data Type**</span></span>|<span data-ttu-id="fa55f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="fa55f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fa55f-112">_Idlang_opt_</span><span class="sxs-lookup"><span data-stu-id="fa55f-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="fa55f-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="fa55f-113">Optional</span></span>  <br/> |<span data-ttu-id="fa55f-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="fa55f-114">**Number**</span></span> <br/> |<span data-ttu-id="fa55f-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="fa55f-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fa55f-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="fa55f-118">Return value</span></span>

<span data-ttu-id="fa55f-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="fa55f-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa55f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa55f-120">Remarks</span></span>

<span data-ttu-id="fa55f-121">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fa55f-121">If you pass an illegal language code, the local language is used.</span></span>
  

