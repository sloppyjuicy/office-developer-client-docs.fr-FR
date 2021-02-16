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
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435837"
---
# <a name="playsound-function"></a><span data-ttu-id="b2570-103">Fonction PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="b2570-103">PLAYSOUND Function</span></span>

<span data-ttu-id="b2570-104">Lit un fichier audio ou un son système.</span><span class="sxs-lookup"><span data-stu-id="b2570-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b2570-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2570-105">Syntax</span></span>

<span data-ttu-id="b2570-106">PLAYSOUND( » \*\* *filename* \*\* « | » \*\* *alias* \*\* « , \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b2570-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b2570-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2570-107">Parameters</span></span>

|<span data-ttu-id="b2570-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b2570-108">**Name**</span></span>|<span data-ttu-id="b2570-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="b2570-109">**Required/Optional**</span></span>|<span data-ttu-id="b2570-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2570-110">**Data Type**</span></span>|<span data-ttu-id="b2570-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2570-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b2570-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="b2570-112">_filename_</span></span> <br/> |<span data-ttu-id="b2570-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2570-113">Required</span></span>  <br/> |<span data-ttu-id="b2570-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b2570-114">**String**</span></span> <br/> |<span data-ttu-id="b2570-115">Nom du fichier audio à lire.</span><span class="sxs-lookup"><span data-stu-id="b2570-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="b2570-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="b2570-116">_alias_</span></span> <br/> |<span data-ttu-id="b2570-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2570-117">Required</span></span>  <br/> |<span data-ttu-id="b2570-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b2570-118">**String**</span></span> <br/> | <span data-ttu-id="b2570-119">Son système représenté par un alias.</span><span class="sxs-lookup"><span data-stu-id="b2570-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="b2570-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="b2570-120">_isAlias_</span></span> <br/> |<span data-ttu-id="b2570-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2570-121">Required</span></span>  <br/> |<span data-ttu-id="b2570-122">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="b2570-122">**Boolean**</span></span> <br/> | <span data-ttu-id="b2570-123">Indique si l’expression précédente est un alias ou un nom de fichier ; une valeur non nulle est un alias.</span><span class="sxs-lookup"><span data-stu-id="b2570-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="b2570-124">_beep_</span><span class="sxs-lookup"><span data-stu-id="b2570-124">_beep_</span></span> <br/> |<span data-ttu-id="b2570-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2570-125">Required</span></span>  <br/> |<span data-ttu-id="b2570-126">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="b2570-126">**Boolean**</span></span> <br/> |<span data-ttu-id="b2570-127">Microsoft Visio émet un signal sonore s’il n’arrive pas à lire le son ; une valeur non nulle active le signal sonore.</span><span class="sxs-lookup"><span data-stu-id="b2570-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="b2570-128">_synch_</span><span class="sxs-lookup"><span data-stu-id="b2570-128">_synch_</span></span> <br/> |<span data-ttu-id="b2570-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2570-129">Required</span></span>  <br/> |<span data-ttu-id="b2570-130">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="b2570-130">**Boolean**</span></span> <br/> |<span data-ttu-id="b2570-131">Détermine si les sons sont lus de manière asynchrone (0) ou synchrone (1).</span><span class="sxs-lookup"><span data-stu-id="b2570-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2570-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2570-132">Remarks</span></span>

<span data-ttu-id="b2570-133">Vous devez généralement lire les sons de manière asynchrone pour que Visio puisse poursuivre le traitement pendant la lecture du son.</span><span class="sxs-lookup"><span data-stu-id="b2570-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="b2570-134">Pour enchaîner plusieurs sons ensemble, lisez-les de manière synchrone afin d’éviter les échecs de lecture.</span><span class="sxs-lookup"><span data-stu-id="b2570-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b2570-135">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b2570-135">Example 1</span></span>

<span data-ttu-id="b2570-136">PLAYSOUND("piano.wav"; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="b2570-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="b2570-137">Émet le fichier audio piano.wav de façon asynchrone et sans signal d’avertissement en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="b2570-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b2570-138">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b2570-138">Example 2</span></span>

<span data-ttu-id="b2570-139">PLAYSOUND("SystemExclamation"; 1; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="b2570-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="b2570-140">Émet le son système d’exclamation de façon asynchrone et sans signal d’avertissement en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="b2570-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

