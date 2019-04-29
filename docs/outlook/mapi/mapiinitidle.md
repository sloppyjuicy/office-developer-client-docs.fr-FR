---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432442"
---
# <a name="mapiinitidle"></a><span data-ttu-id="fac1f-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="fac1f-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="fac1f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fac1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fac1f-105">Initialise le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="fac1f-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fac1f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fac1f-106">Header file:</span></span>  <br/> |<span data-ttu-id="fac1f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="fac1f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fac1f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="fac1f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fac1f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fac1f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fac1f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="fac1f-110">Called by:</span></span>  <br/> |<span data-ttu-id="fac1f-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fac1f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="fac1f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fac1f-112">Parameters</span></span>

 <span data-ttu-id="fac1f-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="fac1f-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="fac1f-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="fac1f-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fac1f-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fac1f-115">Return value</span></span>

<span data-ttu-id="fac1f-116">La fonction **MAPIInitIdle** renvoie zéro si l'initialisation réussit et 1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fac1f-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="fac1f-117">Si **MAPIInitIdle** est appelé plusieurs fois, tous les appels supplémentaires aboutissent, mais sont ignorés, sauf pour incrémenter le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="fac1f-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fac1f-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="fac1f-118">Remarks</span></span>

<span data-ttu-id="fac1f-119">Une application cliente ou un fournisseur de services doit appeler **MAPIInitIdle** avant d'appeler une autre fonction de moteur inactive.</span><span class="sxs-lookup"><span data-stu-id="fac1f-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="fac1f-120">Chaque appel à **MAPIInitIdle** doit être mis en correspondance par un appel ultérieur à [MAPIDeInitIdle](mapideinitidle.md), ou le moteur inactif est laissé en cours d'exécution pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="fac1f-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="fac1f-121">Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="fac1f-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="fac1f-122">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="fac1f-122">**Idle routine function**</span></span>|<span data-ttu-id="fac1f-123">**Usage**</span><span class="sxs-lookup"><span data-stu-id="fac1f-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fac1f-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="fac1f-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="fac1f-125">Modifie les caractéristiques d'une routine inactive enregistrée.</span><span class="sxs-lookup"><span data-stu-id="fac1f-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="fac1f-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="fac1f-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="fac1f-127">Supprime une routine inactive inscrite du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="fac1f-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="fac1f-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="fac1f-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="fac1f-129">Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="fac1f-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="fac1f-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="fac1f-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="fac1f-131">Ajoute une routine inactive au système MAPI, avec ou sans l'activer.</span><span class="sxs-lookup"><span data-stu-id="fac1f-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="fac1f-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="fac1f-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="fac1f-133">Arrête le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="fac1f-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="fac1f-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="fac1f-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="fac1f-135">Initialise le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="fac1f-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="fac1f-136">Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="fac1f-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="fac1f-137">Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="fac1f-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

