---
title: MASTERNAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Renvoie un nom de feuille maître sous forme de chaîne, ou ne renvoie la chaîne « aucune forme de base » si la feuille ne possède pas une forme de base.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789079"
---
# <a name="mastername-function"></a><span data-ttu-id="b10b0-103">MASTERNAME, fonction</span><span class="sxs-lookup"><span data-stu-id="b10b0-103">MASTERNAME Function</span></span>

<span data-ttu-id="b10b0-104">Renvoie un nom de feuille maître sous forme de chaîne ou la chaîne «\<aucune forme de base\>» si la feuille ne possède pas une forme de base.</span><span class="sxs-lookup"><span data-stu-id="b10b0-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b10b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b10b0-105">Syntax</span></span>

<span data-ttu-id="b10b0-106">MASTERNAME ([** *Idlang_opt* **])</span><span class="sxs-lookup"><span data-stu-id="b10b0-106">MASTERNAME ([ ** *langID_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b10b0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b10b0-107">Parameters</span></span>

|<span data-ttu-id="b10b0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b10b0-108">**Name**</span></span>|<span data-ttu-id="b10b0-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="b10b0-109">**Required/Optional**</span></span>|<span data-ttu-id="b10b0-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b10b0-110">**Data Type**</span></span>|<span data-ttu-id="b10b0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b10b0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b10b0-112">_Idlang_opt_</span><span class="sxs-lookup"><span data-stu-id="b10b0-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="b10b0-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b10b0-113">Optional</span></span>  <br/> |<span data-ttu-id="b10b0-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="b10b0-114">**Number**</span></span> <br/> |<span data-ttu-id="b10b0-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="b10b0-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b10b0-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b10b0-118">Return value</span></span>

<span data-ttu-id="b10b0-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b10b0-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b10b0-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b10b0-120">Remarks</span></span>

<span data-ttu-id="b10b0-121">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="b10b0-121">If you pass an illegal language code, the local language is used.</span></span> 
  

