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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410220"
---
# <a name="enableidleroutine"></a><span data-ttu-id="e6e9c-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e6e9c-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="e6e9c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6e9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6e9c-105">Active ou désactive une routine inactive basée sur [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e9c-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6e9c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e6e9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6e9c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e6e9c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e6e9c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e6e9c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6e9c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6e9c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e6e9c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e6e9c-110">Called by:</span></span>  <br/> |<span data-ttu-id="e6e9c-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e6e9c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="e6e9c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6e9c-112">Parameters</span></span>

 <span data-ttu-id="e6e9c-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="e6e9c-113">_ftg_</span></span>
  
> <span data-ttu-id="e6e9c-114">dans Balise de fonction qui identifie la routine inactive à activer ou à désactiver.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="e6e9c-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="e6e9c-115">_fEnable_</span></span>
  
> <span data-ttu-id="e6e9c-116">dans Contient la valeur TRUE si le moteur inactif doit activer la routine inactive ou FALSe s'il doit le désactiver.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6e9c-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6e9c-117">Return value</span></span>

<span data-ttu-id="e6e9c-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6e9c-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6e9c-119">Remarks</span></span>

<span data-ttu-id="e6e9c-120">Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="e6e9c-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="e6e9c-121">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="e6e9c-121">**Idle routine function**</span></span>|<span data-ttu-id="e6e9c-122">**Usage**</span><span class="sxs-lookup"><span data-stu-id="e6e9c-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6e9c-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e6e9c-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="e6e9c-124">Modifie les caractéristiques d'une routine inactive enregistrée.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="e6e9c-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e6e9c-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="e6e9c-126">Supprime une routine inactive inscrite du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="e6e9c-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="e6e9c-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="e6e9c-128">Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e6e9c-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e6e9c-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="e6e9c-130">Ajoute une routine inactive au système MAPI, avec ou sans l'activer.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="e6e9c-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="e6e9c-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="e6e9c-132">Arrête le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="e6e9c-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="e6e9c-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="e6e9c-134">Initialise le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="e6e9c-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="e6e9c-136">Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="e6e9c-137">Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="e6e9c-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

