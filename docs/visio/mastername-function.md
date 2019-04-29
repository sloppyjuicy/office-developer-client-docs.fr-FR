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
description: Renvoie le nom de la forme de base d'une feuille sous forme de chaîne ou renvoie la chaîne «no Master» si la feuille n'a pas de forme de base.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414752"
---
# <a name="mastername-function"></a><span data-ttu-id="35f22-103">Fonction MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="35f22-103">MASTERNAME Function</span></span>

<span data-ttu-id="35f22-104">Renvoie le nom de la forme de base d'une feuille sous forme de chaîne\<ou renvoie\>la chaîne «aucune forme de base» si la feuille ne possède pas de forme de base.</span><span class="sxs-lookup"><span data-stu-id="35f22-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="35f22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35f22-105">Syntax</span></span>

<span data-ttu-id="35f22-106">MASTERNAME ([\* \* *langID_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="35f22-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="35f22-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35f22-107">Parameters</span></span>

|<span data-ttu-id="35f22-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="35f22-108">**Name**</span></span>|<span data-ttu-id="35f22-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="35f22-109">**Required/Optional**</span></span>|<span data-ttu-id="35f22-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="35f22-110">**Data Type**</span></span>|<span data-ttu-id="35f22-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="35f22-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35f22-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="35f22-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="35f22-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="35f22-113">Optional</span></span>  <br/> |<span data-ttu-id="35f22-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="35f22-114">**Number**</span></span> <br/> |<span data-ttu-id="35f22-p101">Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.</span><span class="sxs-lookup"><span data-stu-id="35f22-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="35f22-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35f22-118">Return value</span></span>

<span data-ttu-id="35f22-119">Chaîne</span><span class="sxs-lookup"><span data-stu-id="35f22-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35f22-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="35f22-120">Remarks</span></span>

<span data-ttu-id="35f22-121">Si vous utilisez un code de langue interdit, la langue locale est utilisée.</span><span class="sxs-lookup"><span data-stu-id="35f22-121">If you pass an illegal language code, the local language is used.</span></span> 
  

