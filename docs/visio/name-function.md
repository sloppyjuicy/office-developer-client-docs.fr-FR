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
description: Renvoie le nom d’une feuille sous forme de chaîne.
ms.openlocfilehash: 0d3a70573177d8e16a16972d0a08245381b209dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789160"
---
# <a name="name-function"></a><span data-ttu-id="ebc41-103">NAME, fonction</span><span class="sxs-lookup"><span data-stu-id="ebc41-103">NAME Function</span></span>

<span data-ttu-id="ebc41-104">Renvoie le nom d’une feuille sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="ebc41-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ebc41-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebc41-105">Syntax</span></span>

<span data-ttu-id="ebc41-106">NOM (** *Idlang_opt* **)</span><span class="sxs-lookup"><span data-stu-id="ebc41-106">NAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ebc41-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc41-107">Parameters</span></span>

|<span data-ttu-id="ebc41-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ebc41-108">**Name**</span></span>|<span data-ttu-id="ebc41-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ebc41-109">**Required/Optional**</span></span>|<span data-ttu-id="ebc41-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ebc41-110">**Data Type**</span></span>|<span data-ttu-id="ebc41-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ebc41-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ebc41-112">_Idlang_opt_</span><span class="sxs-lookup"><span data-stu-id="ebc41-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="ebc41-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="ebc41-113">Optional</span></span>  <br/> |<span data-ttu-id="ebc41-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="ebc41-114">**Number**</span></span> <br/> |<span data-ttu-id="ebc41-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="ebc41-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ebc41-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ebc41-118">Return value</span></span>

<span data-ttu-id="ebc41-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ebc41-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebc41-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebc41-120">Remarks</span></span>

<span data-ttu-id="ebc41-121">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ebc41-121">If you pass an illegal language code, the local language is used.</span></span> 
  

