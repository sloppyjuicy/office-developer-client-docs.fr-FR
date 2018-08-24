---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cbad4b903592f83fc7d72fde21f149c9835f2e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575636"
---
# <a name="fnidle"></a><span data-ttu-id="7a56f-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="7a56f-103">FNIDLE</span></span>
 
<span data-ttu-id="7a56f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a56f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a56f-105">Définit une routine d’inactive le moteur inactif MAPI appelle régulièrement en fonction de la priorité.</span><span class="sxs-lookup"><span data-stu-id="7a56f-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a56f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7a56f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a56f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7a56f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7a56f-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="7a56f-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="7a56f-109">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7a56f-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="7a56f-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="7a56f-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="7a56f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="7a56f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="7a56f-112">Type de pointeur correspondant :</span><span class="sxs-lookup"><span data-stu-id="7a56f-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="7a56f-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="7a56f-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="7a56f-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a56f-114">Parameters</span></span>

 <span data-ttu-id="7a56f-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="7a56f-115">_lpvContext_</span></span>
  
> <span data-ttu-id="7a56f-116">[in] Pointeur vers un bloc de mémoire que MAPI passe à la routine inactive chaque fois qu’il l’appelle.</span><span class="sxs-lookup"><span data-stu-id="7a56f-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="7a56f-117">Ce pointeur est passé au moteur MAPI inactif dans le paramètre _pvIdleParam_ par [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="7a56f-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="7a56f-118">Les données dans le bloc de mémoire peuvent fournir le contexte de l’appel de la routine d’inactivité, tels que les objets à utiliser, ou l’état actuel d’une longue opération.</span><span class="sxs-lookup"><span data-stu-id="7a56f-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a56f-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7a56f-119">Return value</span></span>

<span data-ttu-id="7a56f-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="7a56f-120">FALSE</span></span> 
  
> <span data-ttu-id="7a56f-121">Une routine inactive avec le prototype **FNIDLE** doit renvoient toujours la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="7a56f-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a56f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="7a56f-122">Remarks</span></span>

<span data-ttu-id="7a56f-123">Les fonctionnalités spécifiques de la routine d’inactivité sont déterminée par l’implémentation des applications de client ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="7a56f-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="7a56f-124">Le client ou le fournisseur doit limiter la durée d’exécution de chaque état d’une routine d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="7a56f-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="7a56f-125">Chaque état doit effectuer une quantité minimale de traitement, mettre à jour l’état actuel dans les données de contexte désignées par _lpvContext_et retourner au moteur de MAPI inactif.</span><span class="sxs-lookup"><span data-stu-id="7a56f-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="7a56f-126">Le client ou le fournisseur doit appeler la fonction MAPI [MAPIInitIdle](mapiinitidle.md) avant qu’il peut enregistrer son propre routine inactif par un appel à la fonction [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) .</span><span class="sxs-lookup"><span data-stu-id="7a56f-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="7a56f-127">Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction FNIDLE :</span><span class="sxs-lookup"><span data-stu-id="7a56f-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="7a56f-128">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="7a56f-128">**Idle routine function**</span></span>|<span data-ttu-id="7a56f-129">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="7a56f-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a56f-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7a56f-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="7a56f-131">Modifie les caractéristiques d’une routine d’inactivité inscrit.</span><span class="sxs-lookup"><span data-stu-id="7a56f-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="7a56f-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7a56f-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="7a56f-133">Supprime une routine d’inactivité inscrit dans le système MAPI.</span><span class="sxs-lookup"><span data-stu-id="7a56f-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="7a56f-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7a56f-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="7a56f-135">Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="7a56f-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="7a56f-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="7a56f-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="7a56f-137">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="7a56f-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="7a56f-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="7a56f-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="7a56f-139">Arrête le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="7a56f-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="7a56f-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="7a56f-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="7a56f-141">Initialise le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="7a56f-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="7a56f-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="7a56f-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="7a56f-143">Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="7a56f-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="7a56f-144">Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité.</span><span class="sxs-lookup"><span data-stu-id="7a56f-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

