---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408207"
---
# <a name="mapideinitidle"></a><span data-ttu-id="919a8-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="919a8-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="919a8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="919a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="919a8-105">Arrête le moteur d’inactivité MAPI pour l’application à l’appel.</span><span class="sxs-lookup"><span data-stu-id="919a8-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="919a8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="919a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="919a8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="919a8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="919a8-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="919a8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="919a8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="919a8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="919a8-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="919a8-110">Called by:</span></span>  <br/> |<span data-ttu-id="919a8-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="919a8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="919a8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="919a8-112">Parameters</span></span>

<span data-ttu-id="919a8-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="919a8-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="919a8-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="919a8-114">Return value</span></span>

<span data-ttu-id="919a8-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="919a8-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="919a8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="919a8-116">Remarks</span></span>

<span data-ttu-id="919a8-117">Une application cliente ou un fournisseur de services doit appeler **MAPIDeInitIdle** lorsqu’il n’a plus besoin du moteur inactif, par exemple, lorsqu’il est sur le point d’arrêter le traitement.</span><span class="sxs-lookup"><span data-stu-id="919a8-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="919a8-118">Chaque appel [à MAPIInitIdle](mapiinitidle.md) doit être suivi d’un appel ultérieur à **MAPIDeInitIdle** ou le moteur inactif reste en cours d’exécution pour l’application d’appel.</span><span class="sxs-lookup"><span data-stu-id="919a8-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="919a8-119">Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="919a8-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="919a8-120">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="919a8-120">**Idle routine function**</span></span>|<span data-ttu-id="919a8-121">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="919a8-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="919a8-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="919a8-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="919a8-123">Modifie les caractéristiques d’une routine inactive inscrite.</span><span class="sxs-lookup"><span data-stu-id="919a8-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="919a8-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="919a8-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="919a8-125">Supprime une routine d’inactivité enregistrée du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="919a8-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="919a8-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="919a8-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="919a8-127">Désactive ou réactive une routine d’inactivité enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="919a8-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="919a8-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="919a8-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="919a8-129">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="919a8-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="919a8-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="919a8-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="919a8-131">Arrête le moteur d’inactivité MAPI pour l’application à l’appel.</span><span class="sxs-lookup"><span data-stu-id="919a8-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="919a8-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="919a8-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="919a8-133">Initialise le moteur d’inactivité MAPI pour l’application à l’appel.</span><span class="sxs-lookup"><span data-stu-id="919a8-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="919a8-134">Lorsque toutes les tâches au premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité la plus prioritaire prête à être exécuté.</span><span class="sxs-lookup"><span data-stu-id="919a8-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="919a8-135">Il n’existe aucune garantie d’appel de l’ordre parmi les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="919a8-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

