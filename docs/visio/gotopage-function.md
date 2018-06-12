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
description: Affiche la page qui contient le nom pagename dans la fenêtre actuellement active.
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788740"
---
# <a name="gotopage-function"></a><span data-ttu-id="7b84f-103">GOTOPAGE, fonction</span><span class="sxs-lookup"><span data-stu-id="7b84f-103">GOTOPAGE Function</span></span>

<span data-ttu-id="7b84f-104">Affiche la page qui contient le nom *pagename* dans la fenêtre actuellement active.</span><span class="sxs-lookup"><span data-stu-id="7b84f-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7b84f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b84f-105">Syntax</span></span>

<span data-ttu-id="7b84f-106">GOTOPAGE (« ** *pagename* ** »)</span><span class="sxs-lookup"><span data-stu-id="7b84f-106">GOTOPAGE(" ** *pagename* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7b84f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b84f-107">Parameters</span></span>

|<span data-ttu-id="7b84f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7b84f-108">**Name**</span></span>|<span data-ttu-id="7b84f-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7b84f-109">**Required/Optional**</span></span>|<span data-ttu-id="7b84f-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7b84f-110">**Data Type**</span></span>|<span data-ttu-id="7b84f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7b84f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7b84f-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="7b84f-112">_pagename_</span></span> <br/> |<span data-ttu-id="7b84f-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7b84f-113">Required</span></span>  <br/> |<span data-ttu-id="7b84f-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b84f-114">**String**</span></span> <br/> |<span data-ttu-id="7b84f-115">Nom de la page à atteindre</span><span class="sxs-lookup"><span data-stu-id="7b84f-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b84f-116">Note</span><span class="sxs-lookup"><span data-stu-id="7b84f-116">Remarks</span></span>

<span data-ttu-id="7b84f-117">Si une fenêtre est déjà la page, cette fenêtre devient active.</span><span class="sxs-lookup"><span data-stu-id="7b84f-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="7b84f-118">Si *pagename* n’existe pas, l’application tente d’accéder à http:// *pagename* /.</span><span class="sxs-lookup"><span data-stu-id="7b84f-118">If  *pagename*  does not exist, the application attempts to navigate to http://  *pagename*  /.</span></span> <span data-ttu-id="7b84f-119">Si Visio opère comme un serveur sur place, la fonction GOTOPAGE n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7b84f-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="7b84f-120">Vous pouvez utiliser la fonction HYPERLINK pour accéder à n’importe quel chemin DOS, UNC ou URL.</span><span class="sxs-lookup"><span data-stu-id="7b84f-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="7b84f-p102">Dans les versions précédentes de Visio, cette fonction s’appelait _GOTOPAGE. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style.</span><span class="sxs-lookup"><span data-stu-id="7b84f-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

