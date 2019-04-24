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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357322"
---
# <a name="mapideinitidle"></a><span data-ttu-id="255f4-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="255f4-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="255f4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="255f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="255f4-105">Arrête le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="255f4-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="255f4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="255f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="255f4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="255f4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="255f4-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="255f4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="255f4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="255f4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="255f4-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="255f4-110">Called by:</span></span>  <br/> |<span data-ttu-id="255f4-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="255f4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="255f4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="255f4-112">Parameters</span></span>

<span data-ttu-id="255f4-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="255f4-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="255f4-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="255f4-114">Return value</span></span>

<span data-ttu-id="255f4-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="255f4-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="255f4-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="255f4-116">Remarks</span></span>

<span data-ttu-id="255f4-117">Une application cliente ou un fournisseur de services doit appeler **MAPIDeInitIdle** lorsqu'il n'a plus besoin du moteur inactif, par exemple lorsqu'il est sur le point d'arrêter le traitement.</span><span class="sxs-lookup"><span data-stu-id="255f4-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="255f4-118">Chaque appel à [MAPIInitIdle](mapiinitidle.md) doit être mis en correspondance par un appel ultérieur à **MAPIDeInitIdle**, ou le moteur inactif est laissé en cours d'exécution pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="255f4-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="255f4-119">Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="255f4-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="255f4-120">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="255f4-120">**Idle routine function**</span></span>|<span data-ttu-id="255f4-121">**Usage**</span><span class="sxs-lookup"><span data-stu-id="255f4-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="255f4-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="255f4-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="255f4-123">Modifie les caractéristiques d'une routine inactive enregistrée.</span><span class="sxs-lookup"><span data-stu-id="255f4-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="255f4-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="255f4-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="255f4-125">Supprime une routine inactive inscrite du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="255f4-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="255f4-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="255f4-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="255f4-127">Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="255f4-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="255f4-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="255f4-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="255f4-129">Ajoute une routine inactive au système MAPI, avec ou sans l'activer.</span><span class="sxs-lookup"><span data-stu-id="255f4-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="255f4-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="255f4-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="255f4-131">Arrête le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="255f4-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="255f4-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="255f4-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="255f4-133">Initialise le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="255f4-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="255f4-134">Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="255f4-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="255f4-135">Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="255f4-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

