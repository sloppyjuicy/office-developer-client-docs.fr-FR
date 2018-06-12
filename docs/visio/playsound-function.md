---
title: PLAYSOUND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Lit un fichier audio ou un son système.
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789276"
---
# <a name="playsound-function"></a><span data-ttu-id="50665-103">PLAYSOUND, fonction</span><span class="sxs-lookup"><span data-stu-id="50665-103">PLAYSOUND Function</span></span>

<span data-ttu-id="50665-104">Lit un fichier audio ou un son système.</span><span class="sxs-lookup"><span data-stu-id="50665-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="50665-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50665-105">Syntax</span></span>

<span data-ttu-id="50665-106">PLAYSOUND (« ** *filename* ** « | » ** *alias* ** », ** *estAlias* **, ** *Bip* **, ** *synch* **)</span><span class="sxs-lookup"><span data-stu-id="50665-106">PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="50665-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50665-107">Parameters</span></span>

|<span data-ttu-id="50665-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="50665-108">**Name**</span></span>|<span data-ttu-id="50665-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="50665-109">**Required/Optional**</span></span>|<span data-ttu-id="50665-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="50665-110">**Data Type**</span></span>|<span data-ttu-id="50665-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="50665-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="50665-112">_nom de fichier_</span><span class="sxs-lookup"><span data-stu-id="50665-112">_filename_</span></span> <br/> |<span data-ttu-id="50665-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50665-113">Required</span></span>  <br/> |<span data-ttu-id="50665-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="50665-114">**String**</span></span> <br/> |<span data-ttu-id="50665-115">Nom du fichier audio à lire.</span><span class="sxs-lookup"><span data-stu-id="50665-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="50665-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="50665-116">_alias_</span></span> <br/> |<span data-ttu-id="50665-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50665-117">Required</span></span>  <br/> |<span data-ttu-id="50665-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="50665-118">**String**</span></span> <br/> | <span data-ttu-id="50665-119">Son système représenté par un alias.</span><span class="sxs-lookup"><span data-stu-id="50665-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="50665-120">_estAlias_</span><span class="sxs-lookup"><span data-stu-id="50665-120">_isAlias_</span></span> <br/> |<span data-ttu-id="50665-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50665-121">Required</span></span>  <br/> |<span data-ttu-id="50665-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="50665-122">**Boolean**</span></span> <br/> | <span data-ttu-id="50665-123">Indique si l’expression précédente est un alias ou un nom de fichier ; une valeur non nulle est un alias.</span><span class="sxs-lookup"><span data-stu-id="50665-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="50665-124">_bip_</span><span class="sxs-lookup"><span data-stu-id="50665-124">_beep_</span></span> <br/> |<span data-ttu-id="50665-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50665-125">Required</span></span>  <br/> |<span data-ttu-id="50665-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="50665-126">**Boolean**</span></span> <br/> |<span data-ttu-id="50665-127">Microsoft Visio émet un signal sonore s’il n’arrive pas à lire le son ; une valeur non nulle active le signal sonore.</span><span class="sxs-lookup"><span data-stu-id="50665-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="50665-128">_synchronisation_</span><span class="sxs-lookup"><span data-stu-id="50665-128">_synch_</span></span> <br/> |<span data-ttu-id="50665-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="50665-129">Required</span></span>  <br/> |<span data-ttu-id="50665-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="50665-130">**Boolean**</span></span> <br/> |<span data-ttu-id="50665-131">Détermine si les sons sont lus de manière asynchrone (0) ou synchrone (1).</span><span class="sxs-lookup"><span data-stu-id="50665-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50665-132">Note</span><span class="sxs-lookup"><span data-stu-id="50665-132">Remarks</span></span>

<span data-ttu-id="50665-133">Vous devez généralement lire les sons asynchrone afin que Visio peut continuer à traiter pendant qu’il lit le son.</span><span class="sxs-lookup"><span data-stu-id="50665-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="50665-134">Pour enchaîner plusieurs sons ensemble, les lire de façon synchrone ou certains ne parvient pas à lire.</span><span class="sxs-lookup"><span data-stu-id="50665-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="50665-135">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="50665-135">Example 1</span></span>

<span data-ttu-id="50665-136">PLAYSOUND("piano.wav"; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="50665-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="50665-137">Émet le fichier audio piano.wav de façon asynchrone et sans signal d’avertissement en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="50665-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="50665-138">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="50665-138">Example 2</span></span>

<span data-ttu-id="50665-139">PLAYSOUND("SystemExclamation"; 1; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="50665-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="50665-140">Émet le son système d’exclamation de façon asynchrone et sans signal d’avertissement en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="50665-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

