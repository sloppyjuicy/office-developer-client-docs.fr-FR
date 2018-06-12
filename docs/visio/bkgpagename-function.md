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
description: Renvoie le nom d’une page d’arrière-plan sous forme de chaîne.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788151"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="8995c-103">BKGPAGENAME, fonction</span><span class="sxs-lookup"><span data-stu-id="8995c-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="8995c-104">Renvoie le nom d’une page d’arrière-plan sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8995c-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8995c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8995c-105">Syntax</span></span>

<span data-ttu-id="8995c-106">BKGPAGENAME (** *Idlang_opt* **)</span><span class="sxs-lookup"><span data-stu-id="8995c-106">BKGPAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8995c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8995c-107">Parameters</span></span>

|<span data-ttu-id="8995c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8995c-108">**Name**</span></span>|<span data-ttu-id="8995c-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8995c-109">**Required/Optional**</span></span>|<span data-ttu-id="8995c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8995c-110">**Data Type**</span></span>|<span data-ttu-id="8995c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8995c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8995c-112">_Idlang_opt_</span><span class="sxs-lookup"><span data-stu-id="8995c-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="8995c-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="8995c-113">Optional</span></span>  <br/> |<span data-ttu-id="8995c-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8995c-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8995c-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="8995c-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8995c-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8995c-118">Return value</span></span>

<span data-ttu-id="8995c-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8995c-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8995c-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8995c-120">Remarks</span></span>

<span data-ttu-id="8995c-121">Si la page pour laquelle vous utilisez la fonction ne possède pas une page d’arrière-plan, la chaîne «\<aucun arrière-plan\>» est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="8995c-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="8995c-122">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8995c-122">If you pass an illegal language code, the local language is used.</span></span> 
  

