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
ms.openlocfilehash: fd9a91b089bb06e6dfe34a1a144245d404adb270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569224"
---
# <a name="mapiinitidle"></a><span data-ttu-id="e8253-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="e8253-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="e8253-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8253-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8253-105">Initialise le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="e8253-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8253-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e8253-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8253-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e8253-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e8253-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e8253-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e8253-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e8253-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e8253-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e8253-110">Called by:</span></span>  <br/> |<span data-ttu-id="e8253-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e8253-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="e8253-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8253-112">Parameters</span></span>

 <span data-ttu-id="e8253-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="e8253-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="e8253-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="e8253-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8253-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8253-115">Return value</span></span>

<span data-ttu-id="e8253-116">La fonction **MAPIInitIdle** renvoie zéro si l’initialisation réussit et 1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e8253-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="e8253-117">Si **MAPIInitIdle** est appelée plusieurs fois, tous les appels supplémentaires réussissent, mais sont ignorés sauf to incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="e8253-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8253-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8253-118">Remarks</span></span>

<span data-ttu-id="e8253-119">Une application cliente ou un fournisseur de services doit appeler **MAPIInitIdle** avant d’appeler toute autre fonction moteur inactif.</span><span class="sxs-lookup"><span data-stu-id="e8253-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="e8253-120">Chaque appel à **MAPIInitIdle** doit correspondre à un autre appel à [MAPIDeInitIdle](mapideinitidle.md), ou le moteur d’inactivité est de gauche en cours d’exécution pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="e8253-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="e8253-121">Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="e8253-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="e8253-122">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="e8253-122">**Idle routine function**</span></span>|<span data-ttu-id="e8253-123">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="e8253-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8253-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e8253-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="e8253-125">Modifie les caractéristiques d’une routine d’inactivité inscrit.</span><span class="sxs-lookup"><span data-stu-id="e8253-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="e8253-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e8253-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="e8253-127">Supprime une routine d’inactivité inscrit dans le système MAPI.</span><span class="sxs-lookup"><span data-stu-id="e8253-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e8253-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e8253-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="e8253-129">Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="e8253-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e8253-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e8253-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="e8253-131">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="e8253-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="e8253-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="e8253-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="e8253-133">Arrête le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="e8253-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="e8253-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="e8253-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="e8253-135">Initialise le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="e8253-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="e8253-136">Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="e8253-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="e8253-137">Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité.</span><span class="sxs-lookup"><span data-stu-id="e8253-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

