---
title: NAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Renvoie le nom d'une feuille sous forme de chaîne.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416796"
---
# <a name="name-function"></a><span data-ttu-id="87bd7-103">Fonction NAME</span><span class="sxs-lookup"><span data-stu-id="87bd7-103">NAME Function</span></span>

<span data-ttu-id="87bd7-104">Renvoie le nom d'une feuille sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="87bd7-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="87bd7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87bd7-105">Syntax</span></span>

<span data-ttu-id="87bd7-106">NOM (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="87bd7-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="87bd7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87bd7-107">Parameters</span></span>

|<span data-ttu-id="87bd7-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="87bd7-108">**Name**</span></span>|<span data-ttu-id="87bd7-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="87bd7-109">**Required/Optional**</span></span>|<span data-ttu-id="87bd7-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="87bd7-110">**Data Type**</span></span>|<span data-ttu-id="87bd7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="87bd7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="87bd7-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="87bd7-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="87bd7-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="87bd7-113">Optional</span></span>  <br/> |<span data-ttu-id="87bd7-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="87bd7-114">**Number**</span></span> <br/> |<span data-ttu-id="87bd7-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="87bd7-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="87bd7-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="87bd7-118">Return value</span></span>

<span data-ttu-id="87bd7-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="87bd7-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87bd7-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="87bd7-120">Remarks</span></span>

<span data-ttu-id="87bd7-121">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="87bd7-121">If you pass an illegal language code, the local language is used.</span></span> 
  

