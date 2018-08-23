---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c53bd63e60281e999d0d379913b3609e9472a40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579276"
---
# <a name="enableidleroutine"></a><span data-ttu-id="5835c-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5835c-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="5835c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5835c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5835c-105">Active ou désactive une routine inactive [FNIDLE](fnidle.md) en fonction de.</span><span class="sxs-lookup"><span data-stu-id="5835c-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5835c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5835c-106">Header file:</span></span>  <br/> |<span data-ttu-id="5835c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5835c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5835c-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="5835c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5835c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5835c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5835c-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="5835c-110">Called by:</span></span>  <br/> |<span data-ttu-id="5835c-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5835c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="5835c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5835c-112">Parameters</span></span>

 <span data-ttu-id="5835c-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="5835c-113">_ftg_</span></span>
  
> <span data-ttu-id="5835c-114">[in] Balise de fonction qui identifie la routine inactive pour être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="5835c-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="5835c-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="5835c-115">_fEnable_</span></span>
  
> <span data-ttu-id="5835c-116">[in] Contient la valeur TRUE si le moteur d’inactivité doit activer la routine inactive, ou FALSE si elle doit le désactiver.</span><span class="sxs-lookup"><span data-stu-id="5835c-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5835c-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5835c-117">Return value</span></span>

<span data-ttu-id="5835c-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5835c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5835c-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="5835c-119">Remarks</span></span>

<span data-ttu-id="5835c-120">Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="5835c-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="5835c-121">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="5835c-121">**Idle routine function**</span></span>|<span data-ttu-id="5835c-122">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="5835c-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5835c-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5835c-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="5835c-124">Modifie les caractéristiques d’une routine d’inactivité inscrit.</span><span class="sxs-lookup"><span data-stu-id="5835c-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="5835c-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5835c-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="5835c-126">Supprime une routine d’inactivité inscrit dans le système MAPI.</span><span class="sxs-lookup"><span data-stu-id="5835c-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="5835c-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="5835c-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="5835c-128">Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="5835c-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5835c-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5835c-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="5835c-130">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="5835c-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="5835c-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="5835c-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="5835c-132">Arrête le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="5835c-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="5835c-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="5835c-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="5835c-134">Initialise le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="5835c-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="5835c-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="5835c-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="5835c-136">Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="5835c-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="5835c-137">Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité.</span><span class="sxs-lookup"><span data-stu-id="5835c-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

