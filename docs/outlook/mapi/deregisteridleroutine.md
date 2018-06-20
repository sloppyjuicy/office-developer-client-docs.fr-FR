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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 85161fb87e798bbb03b267f9760870da1246e48d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783155"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="b0eb7-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b0eb7-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="b0eb7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0eb7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0eb7-105">Supprime un [FNIDLE](fnidle.md) en fonction de routine inactive à partir du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0eb7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b0eb7-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0eb7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b0eb7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b0eb7-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="b0eb7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b0eb7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b0eb7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b0eb7-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="b0eb7-110">Called by:</span></span>  <br/> |<span data-ttu-id="b0eb7-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b0eb7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="b0eb7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0eb7-112">Parameters</span></span>

 <span data-ttu-id="b0eb7-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="b0eb7-113">_ftg_</span></span>
  
> <span data-ttu-id="b0eb7-114">[in] Balise de fonction qui identifie la routine inactive à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0eb7-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0eb7-115">Return value</span></span>

<span data-ttu-id="b0eb7-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0eb7-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0eb7-117">Remarks</span></span>

<span data-ttu-id="b0eb7-118">Une tâche dans une application cliente ou d’un fournisseur de services peut annuler l’enregistrement d’une routine inactive pour lequel elle possède un paramètre valide _ftg_ .</span><span class="sxs-lookup"><span data-stu-id="b0eb7-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="b0eb7-119">En particulier, une routine inactive peut désinscrire lui-même.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="b0eb7-120">Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="b0eb7-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="b0eb7-121">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="b0eb7-121">**Idle routine function**</span></span>|<span data-ttu-id="b0eb7-122">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="b0eb7-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0eb7-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b0eb7-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="b0eb7-124">Modifie les caractéristiques d’une routine d’inactivité inscrit.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="b0eb7-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="b0eb7-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="b0eb7-126">Supprime une routine d’inactivité inscrit dans le système MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="b0eb7-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b0eb7-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="b0eb7-128">Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="b0eb7-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="b0eb7-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="b0eb7-130">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="b0eb7-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="b0eb7-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="b0eb7-132">Arrête le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="b0eb7-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="b0eb7-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="b0eb7-134">Initialise le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="b0eb7-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="b0eb7-136">Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="b0eb7-137">Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="b0eb7-138">Une fois la routine inactive inscription est désactivée, le moteur d’inactivité n’appelle pas il à nouveau.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="b0eb7-139">Une implémentation qui appelle **DeregisterIdleRoutine** doit libérer tous les blocs de mémoire à laquelle il passé pointeurs moteur inactif à utiliser dans son appel à la fonction **FtgRegisterIdleRoutine** d’origine.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

