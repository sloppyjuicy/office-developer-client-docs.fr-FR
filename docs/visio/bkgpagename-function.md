---
title: BKGPAGENAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Renvoie un nom de page d'arrière-plan sous forme de chaîne.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410314"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="11272-103">Fonction BKGPAGENAME</span><span class="sxs-lookup"><span data-stu-id="11272-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="11272-104">Renvoie un nom de page d'arrière-plan sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="11272-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="11272-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11272-105">Syntax</span></span>

<span data-ttu-id="11272-106">BKGPAGENAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="11272-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="11272-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11272-107">Parameters</span></span>

|<span data-ttu-id="11272-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="11272-108">**Name**</span></span>|<span data-ttu-id="11272-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="11272-109">**Required/Optional**</span></span>|<span data-ttu-id="11272-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="11272-110">**Data Type**</span></span>|<span data-ttu-id="11272-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="11272-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="11272-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="11272-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="11272-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="11272-113">Optional</span></span>  <br/> |<span data-ttu-id="11272-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="11272-114">**Numeric**</span></span> <br/> |<span data-ttu-id="11272-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="11272-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="11272-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11272-118">Return value</span></span>

<span data-ttu-id="11272-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="11272-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11272-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="11272-120">Remarks</span></span>

<span data-ttu-id="11272-121">Si la page pour laquelle vous utilisez la fonction n'a pas de page d'arrière-plan,\<la chaîne\>«aucun arrière-plan» est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="11272-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="11272-122">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="11272-122">If you pass an illegal language code, the local language is used.</span></span> 
  

