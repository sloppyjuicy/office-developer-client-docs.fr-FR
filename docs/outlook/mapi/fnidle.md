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
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412379"
---
# <a name="fnidle"></a><span data-ttu-id="ade63-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="ade63-103">FNIDLE</span></span>
 
<span data-ttu-id="ade63-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ade63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ade63-105">Définit une routine inactive appelée périodiquement par le moteur inactif MAPI en fonction de la priorité.</span><span class="sxs-lookup"><span data-stu-id="ade63-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ade63-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ade63-106">Header file:</span></span>  <br/> |<span data-ttu-id="ade63-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ade63-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ade63-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="ade63-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="ade63-109">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="ade63-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="ade63-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="ade63-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="ade63-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ade63-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="ade63-112">Type de pointeur correspondant:</span><span class="sxs-lookup"><span data-stu-id="ade63-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="ade63-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="ade63-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="ade63-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ade63-114">Parameters</span></span>

 <span data-ttu-id="ade63-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="ade63-115">_lpvContext_</span></span>
  
> <span data-ttu-id="ade63-116">dans Pointeur vers un bloc de mémoire que MAPI transmet à la routine inactive chaque fois qu'il l'appelle.</span><span class="sxs-lookup"><span data-stu-id="ade63-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="ade63-117">Ce pointeur est transmis au moteur inactif MAPI dans le paramètre _pvIdleParam_ par [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span><span class="sxs-lookup"><span data-stu-id="ade63-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="ade63-118">Les données du bloc de mémoire peuvent fournir un contexte pour l'appel à la routine inactive, par exemple l'objet sur lequel agir, ou l'état actuel d'une longue opération.</span><span class="sxs-lookup"><span data-stu-id="ade63-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ade63-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ade63-119">Return value</span></span>

<span data-ttu-id="ade63-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="ade63-120">FALSE</span></span> 
  
> <span data-ttu-id="ade63-121">Une routine inactive avec le prototype **FNIDLE** doit toujours renvoyer la valeur false.</span><span class="sxs-lookup"><span data-stu-id="ade63-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ade63-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="ade63-122">Remarks</span></span>

<span data-ttu-id="ade63-123">La fonctionnalité spécifique de la routine inactive est déterminée par l'application cliente ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ade63-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="ade63-124">Le client ou le fournisseur doit limiter le temps d'exécution de chaque État d'une routine inactive.</span><span class="sxs-lookup"><span data-stu-id="ade63-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="ade63-125">Chaque État doit effectuer une quantité minimale de traitement, mettre à jour l'état actuel dans les données de contexte pointées par _lpvContext_, puis revenir au moteur d'inactivité MAPI.</span><span class="sxs-lookup"><span data-stu-id="ade63-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="ade63-126">Le client ou le fournisseur doit appeler la fonction MAPI [MAPIInitIdle](mapiinitidle.md) pour pouvoir inscrire sa propre routine inactive avec un appel à la fonction [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) .</span><span class="sxs-lookup"><span data-stu-id="ade63-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="ade63-127">Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction FNIDLE:</span><span class="sxs-lookup"><span data-stu-id="ade63-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="ade63-128">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="ade63-128">**Idle routine function**</span></span>|<span data-ttu-id="ade63-129">**Usage**</span><span class="sxs-lookup"><span data-stu-id="ade63-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ade63-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ade63-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="ade63-131">Modifie les caractéristiques d'une routine inactive enregistrée.</span><span class="sxs-lookup"><span data-stu-id="ade63-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="ade63-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ade63-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="ade63-133">Supprime une routine inactive inscrite du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="ade63-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="ade63-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ade63-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="ade63-135">Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="ade63-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="ade63-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ade63-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="ade63-137">Ajoute une routine inactive au système MAPI, avec ou sans l'activer.</span><span class="sxs-lookup"><span data-stu-id="ade63-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="ade63-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="ade63-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="ade63-139">Arrête le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="ade63-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="ade63-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="ade63-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="ade63-141">Initialise le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="ade63-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="ade63-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="ade63-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="ade63-143">Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="ade63-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="ade63-144">Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="ade63-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

