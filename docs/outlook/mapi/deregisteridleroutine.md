---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404560"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="689aa-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="689aa-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="689aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="689aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="689aa-105">Supprime une routine [d’inactivité basée sur FNIDLE](fnidle.md) du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="689aa-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="689aa-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="689aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="689aa-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="689aa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="689aa-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="689aa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="689aa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="689aa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="689aa-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="689aa-110">Called by:</span></span>  <br/> |<span data-ttu-id="689aa-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="689aa-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="689aa-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="689aa-112">Parameters</span></span>

 <span data-ttu-id="689aa-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="689aa-113">_ftg_</span></span>
  
> <span data-ttu-id="689aa-114">[in] Balise de fonction qui identifie la routine inactive à supprimer.</span><span class="sxs-lookup"><span data-stu-id="689aa-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="689aa-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="689aa-115">Return value</span></span>

<span data-ttu-id="689aa-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="689aa-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="689aa-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="689aa-117">Remarks</span></span>

<span data-ttu-id="689aa-118">Toute tâche d’une application cliente ou d’un fournisseur de services peut désinserrez toute routine inactive pour laquelle elle possède un paramètre  _ftg_ valide.</span><span class="sxs-lookup"><span data-stu-id="689aa-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="689aa-119">En particulier, une routine inactive peut se désins inscrit elle-même.</span><span class="sxs-lookup"><span data-stu-id="689aa-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="689aa-120">Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="689aa-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="689aa-121">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="689aa-121">**Idle routine function**</span></span>|<span data-ttu-id="689aa-122">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="689aa-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="689aa-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="689aa-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="689aa-124">Modifie les caractéristiques d’une routine d’inactivité inscrite.</span><span class="sxs-lookup"><span data-stu-id="689aa-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="689aa-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="689aa-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="689aa-126">Supprime une routine d’inactivité enregistrée du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="689aa-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="689aa-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="689aa-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="689aa-128">Désactive ou réactive une routine d’inactivité enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="689aa-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="689aa-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="689aa-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="689aa-130">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="689aa-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="689aa-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="689aa-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="689aa-132">Arrête le moteur d’inactivité MAPI pour l’application à l’appel.</span><span class="sxs-lookup"><span data-stu-id="689aa-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="689aa-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="689aa-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="689aa-134">Initialise le moteur d’inactivité MAPI pour l’application à l’appel.</span><span class="sxs-lookup"><span data-stu-id="689aa-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="689aa-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine** et **EnableIdleRoutine** prennent comme paramètre d’entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="689aa-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="689aa-136">Lorsque toutes les tâches au premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité la plus prioritaire prête à être exécuté.</span><span class="sxs-lookup"><span data-stu-id="689aa-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="689aa-137">Il n’existe aucune garantie d’appel d’ordre parmi les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="689aa-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="689aa-138">Une fois la routine inactive désinserrée, le moteur inactif ne l’appelle plus.</span><span class="sxs-lookup"><span data-stu-id="689aa-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="689aa-139">Toute implémentation qui appelle **DeregisterIdleRoutine** doit désaffecter les blocs de mémoire vers lesquels elle a passé des pointeurs pour que le moteur inactif utilise dans son appel d’origine à la fonction **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="689aa-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

