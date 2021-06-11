---
title: GOTOPAGE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Affiche la page dont le nom est nom dans la fenêtre active.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302967"
---
# <a name="gotopage-function"></a><span data-ttu-id="8e0d0-103">Fonction GOTOPAGE</span><span class="sxs-lookup"><span data-stu-id="8e0d0-103">GOTOPAGE Function</span></span>

<span data-ttu-id="8e0d0-104">Affiche la page dont le nom est  *nom dans*  la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8e0d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e0d0-105">Syntax</span></span>

<span data-ttu-id="8e0d0-106">GOTOPAGE( » \*\* *pagename* \*\* « )</span><span class="sxs-lookup"><span data-stu-id="8e0d0-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8e0d0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e0d0-107">Parameters</span></span>

|<span data-ttu-id="8e0d0-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8e0d0-108">**Name**</span></span>|<span data-ttu-id="8e0d0-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8e0d0-109">**Required/Optional**</span></span>|<span data-ttu-id="8e0d0-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8e0d0-110">**Data Type**</span></span>|<span data-ttu-id="8e0d0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8e0d0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8e0d0-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="8e0d0-112">_pagename_</span></span> <br/> |<span data-ttu-id="8e0d0-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8e0d0-113">Required</span></span>  <br/> |<span data-ttu-id="8e0d0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8e0d0-114">**String**</span></span> <br/> |<span data-ttu-id="8e0d0-115">Nom de la page à atteindre</span><span class="sxs-lookup"><span data-stu-id="8e0d0-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e0d0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e0d0-116">Remarks</span></span>

<span data-ttu-id="8e0d0-117">Si la page est déjà ouverte dans une fenêtre, cette fenêtre est activée.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="8e0d0-118">Si  *le nom de page n’existe*  pas, l’application tente d’accéder https://  *pagename*  /.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="8e0d0-119">Si Visio opère comme un serveur de modification sur place, la fonction GOTOPAGE n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="8e0d0-120">Vous pouvez utiliser la fonction HYPERLINK pour accéder à n’importe quel chemin DOS, UNC ou URL.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="8e0d0-p102">Dans les versions précédentes de Visio, cette fonction s’appelait _GOTOPAGE. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

