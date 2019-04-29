---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418266"
---
# <a name="changeidleroutine"></a><span data-ttu-id="c791c-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c791c-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="c791c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c791c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c791c-105">Modifie une partie ou l'ensemble des caractéristiques d'une routine inactive basée sur [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="c791c-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c791c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c791c-106">Header file:</span></span>  <br/> |<span data-ttu-id="c791c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="c791c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c791c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c791c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c791c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c791c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c791c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c791c-110">Called by:</span></span>  <br/> |<span data-ttu-id="c791c-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="c791c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a><span data-ttu-id="c791c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c791c-112">Parameters</span></span>

<span data-ttu-id="c791c-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="c791c-113">_ftg_</span></span>
  
> <span data-ttu-id="c791c-114">dans Balise de fonction qui identifie la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="c791c-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="c791c-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="c791c-116">dans Pointeur vers la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="c791c-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="c791c-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="c791c-118">dans Pointeur vers un nouveau bloc de mémoire que l'implémentation d'appel alloue pour la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="c791c-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="c791c-119">_priIdle_</span></span>
  
> <span data-ttu-id="c791c-120">dans Valeur représentant une nouvelle priorité pour la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="c791c-121">Les priorités possibles pour les routines définies par l'implémentation sont supérieures ou inférieures à zéro, mais pas à zéro.</span><span class="sxs-lookup"><span data-stu-id="c791c-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="c791c-122">La valeur zéro est réservée à un événement utilisateur tel qu'un clic de souris ou un message WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="c791c-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="c791c-123">Les valeurs supérieures à zéro représentent des priorités pour les tâches d'arrière-plan dont la priorité est supérieure à celle des événements utilisateur et qui sont distribuées dans le cadre de la boucle Windows message Pump standard.</span><span class="sxs-lookup"><span data-stu-id="c791c-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="c791c-124">Les valeurs inférieures à zéro représentent des priorités pour les tâches inactives qui s'exécutent uniquement pendant la durée d'inactivité de la pompe de messages.</span><span class="sxs-lookup"><span data-stu-id="c791c-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="c791c-125">Exemples de priorités: 1 pour l'envoi de premier plan, 1 pour l'insertion de caractères de modification de l'alimentation et 3 pour le téléchargement de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="c791c-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="c791c-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="c791c-126">_csecIdle_</span></span>
  
> <span data-ttu-id="c791c-127">dans Une nouvelle heure, en centièmes de seconde, à appliquer à la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="c791c-128">La signification de la valeur de l'heure initiale varie en fonction de ce qui est passé dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="c791c-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="c791c-129">Il peut s'agir des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c791c-129">It can be:</span></span> 
    
  - <span data-ttu-id="c791c-130">Période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur inactif MAPI appelle la routine inactive pour la première fois, si l'indicateur FIROWAIT est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="c791c-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="c791c-131">Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c791c-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="c791c-132">Intervalle minimal entre les appels à la routine inactive, si l'indicateur FIROINTERVAL est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="c791c-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="c791c-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="c791c-133">_iroIdle_</span></span>
  
> <span data-ttu-id="c791c-134">dans Masque de des indicateurs indiquant les nouvelles options d'appel de la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="c791c-135">Exactement l'un des indicateurs suivants doit être défini:</span><span class="sxs-lookup"><span data-stu-id="c791c-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="c791c-136">FIROINTERVAL: le temps spécifié par le paramètre _csecIdle_ est l'intervalle minimal entre les appels successifs de la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="c791c-137">FIROONCEONLY: obsolète.</span><span class="sxs-lookup"><span data-stu-id="c791c-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="c791c-138">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="c791c-138">Do not use.</span></span> 
      
  - <span data-ttu-id="c791c-139">FIROPERBLOCK: obsolète.</span><span class="sxs-lookup"><span data-stu-id="c791c-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="c791c-140">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="c791c-140">Do not use.</span></span> 
      
  - <span data-ttu-id="c791c-141">FIROWAIT: le temps spécifié par le paramètre _csecIdle_ est la période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur d'inactivité MAPI appelle la routine inactive pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="c791c-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="c791c-142">Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c791c-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="c791c-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="c791c-143">_ircIdle_</span></span>
  
> <span data-ttu-id="c791c-144">dans Masque de des indicateurs utilisé pour indiquer les modifications à apporter à la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="c791c-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="c791c-145">Les indicateurs suivants peuvent être définis dans n'importe quelle combinaison:</span><span class="sxs-lookup"><span data-stu-id="c791c-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="c791c-146">FIRCCSEC: modification de l'heure associée à la routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _csecIdle_ .</span><span class="sxs-lookup"><span data-stu-id="c791c-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c791c-147">FIRCIRO: modification des options de la routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="c791c-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c791c-148">FIRCPFN: modification du pointeur de routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _pfnIdle_ .</span><span class="sxs-lookup"><span data-stu-id="c791c-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c791c-149">FIRCPRI: modification de la priorité de la routine inactive, c'est-à-dire d'une modification indiquée par la valeur transmise dans le paramètre _priIdle_ .</span><span class="sxs-lookup"><span data-stu-id="c791c-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="c791c-150">FIRCPV: modification du bloc de mémoire de la routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _pvIdleParam_ .</span><span class="sxs-lookup"><span data-stu-id="c791c-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c791c-151">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c791c-151">Return value</span></span>

<span data-ttu-id="c791c-152">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c791c-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c791c-153">Remarques</span><span class="sxs-lookup"><span data-stu-id="c791c-153">Remarks</span></span>

<span data-ttu-id="c791c-154">Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="c791c-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="c791c-155">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="c791c-155">**Idle routine function**</span></span>|<span data-ttu-id="c791c-156">**Usage**</span><span class="sxs-lookup"><span data-stu-id="c791c-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c791c-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="c791c-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="c791c-158">Modifie les caractéristiques d'une routine inactive enregistrée.</span><span class="sxs-lookup"><span data-stu-id="c791c-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="c791c-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c791c-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="c791c-160">Supprime une routine inactive inscrite du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="c791c-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="c791c-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c791c-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="c791c-162">Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="c791c-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="c791c-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="c791c-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="c791c-164">Ajoute une routine inactive au système MAPI, avec ou sans l'activer.</span><span class="sxs-lookup"><span data-stu-id="c791c-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="c791c-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="c791c-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="c791c-166">Arrête le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="c791c-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="c791c-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="c791c-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="c791c-168">Initialise le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="c791c-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="c791c-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="c791c-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="c791c-170">Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="c791c-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="c791c-171">Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="c791c-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

