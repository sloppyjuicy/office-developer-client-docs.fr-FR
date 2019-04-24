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
description: Renvoie le nom de la page sous la forme d'une chaîne.
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339464"
---
# <a name="pagename-function"></a><span data-ttu-id="9c793-103">Fonction PAGENAME</span><span class="sxs-lookup"><span data-stu-id="9c793-103">PAGENAME Function</span></span>

<span data-ttu-id="9c793-104">Renvoie le nom de la page sous la forme d'une chaîne.</span><span class="sxs-lookup"><span data-stu-id="9c793-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9c793-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c793-105">Syntax</span></span>

<span data-ttu-id="9c793-106">PAGENAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9c793-106">PAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9c793-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c793-107">Parameters</span></span>

|<span data-ttu-id="9c793-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9c793-108">**Name**</span></span>|<span data-ttu-id="9c793-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9c793-109">**Required/Optional**</span></span>|<span data-ttu-id="9c793-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9c793-110">**Data Type**</span></span>|<span data-ttu-id="9c793-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c793-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9c793-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="9c793-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="9c793-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="9c793-113">Optional</span></span>  <br/> |<span data-ttu-id="9c793-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="9c793-114">**Number**</span></span> <br/> |<span data-ttu-id="9c793-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="9c793-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9c793-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9c793-118">Return value</span></span>

<span data-ttu-id="9c793-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9c793-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c793-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="9c793-120">Remarks</span></span>

<span data-ttu-id="9c793-121">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9c793-121">If you pass an illegal language code, the local language is used.</span></span>
  

