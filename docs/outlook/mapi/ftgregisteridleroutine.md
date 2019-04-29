---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418520"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="48a12-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a12-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="48a12-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48a12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48a12-105">Ajoute une routine inactive basée sur la fonction [FNIDLE](fnidle.md) au système MAPI.</span><span class="sxs-lookup"><span data-stu-id="48a12-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48a12-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="48a12-106">Header file:</span></span>  <br/> |<span data-ttu-id="48a12-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="48a12-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="48a12-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="48a12-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48a12-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48a12-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48a12-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="48a12-110">Called by:</span></span>  <br/> |<span data-ttu-id="48a12-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="48a12-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="48a12-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48a12-112">Parameters</span></span>

<span data-ttu-id="48a12-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="48a12-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="48a12-114">dans Pointeur vers la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="48a12-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="48a12-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="48a12-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="48a12-116">dans Pointeur vers un bloc de mémoire que le moteur inactif doit transmettre en tant que paramètre à la routine inactive lorsqu'il l'appelle.</span><span class="sxs-lookup"><span data-stu-id="48a12-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="48a12-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="48a12-117">_priIdle_</span></span>
  
> <span data-ttu-id="48a12-118">dans Priorité initiale de la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="48a12-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="48a12-119">Les priorités possibles pour les routines définies par l'implémentation sont supérieures ou inférieures à zéro, mais pas à zéro.</span><span class="sxs-lookup"><span data-stu-id="48a12-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="48a12-120">La priorité zéro est réservée à un événement utilisateur tel qu'un clic de souris ou un message WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="48a12-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="48a12-121">Les priorités supérieures à zéro représentent les tâches en arrière-plan dont la priorité est supérieure à celle des événements utilisateur et qui sont distribuées dans le cadre de la boucle Windows message Pump standard.</span><span class="sxs-lookup"><span data-stu-id="48a12-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="48a12-122">Les priorités inférieures à zéro représentent des tâches inactives qui s'exécutent uniquement pendant la durée d'inactivité de la pompe de messages.</span><span class="sxs-lookup"><span data-stu-id="48a12-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="48a12-123">Voici des exemples de priorités: 1 pour l'envoi de premier plan, 2 pour l'insertion de caractères de modification de l'alimentation et 3 pour le téléchargement de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="48a12-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="48a12-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="48a12-124">_csecIdle_</span></span>
  
> <span data-ttu-id="48a12-125">dans Valeur de l'heure initiale, en centièmes de seconde, à utiliser pour spécifier les paramètres de routine inactive.</span><span class="sxs-lookup"><span data-stu-id="48a12-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="48a12-126">La signification de la valeur de l'heure initiale varie en fonction de ce qui est passé dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="48a12-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="48a12-127">La signification peut être l'une des suivantes:</span><span class="sxs-lookup"><span data-stu-id="48a12-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="48a12-128">Période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur inactif MAPI appelle la routine inactive pour la première fois, si l'indicateur FIROWAIT est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="48a12-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="48a12-129">Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="48a12-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="48a12-130">Intervalle minimal entre les appels à la routine inactive, si l'indicateur FIROINTERVAL est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="48a12-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="48a12-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="48a12-131">_iroIdle_</span></span>
  
> <span data-ttu-id="48a12-132">dans Masque de réinitialisation des indicateurs utilisés pour définir les options initiales de la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="48a12-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="48a12-133">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="48a12-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="48a12-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="48a12-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="48a12-135">Utilisez cet indicateur pour spécifier que le minuteur de la routine inactive ne doit pas être ajusté en mode veille ou reprise.</span><span class="sxs-lookup"><span data-stu-id="48a12-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="48a12-136">Le comportement par défaut sans cet indicateur est que le temps de sommeil est exclu lors du calcul du temps écoulé.</span><span class="sxs-lookup"><span data-stu-id="48a12-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="48a12-137">Si FIRONOADJUSTMENT est transmis, la durée de veille est incluse lors du calcul du temps écoulé.</span><span class="sxs-lookup"><span data-stu-id="48a12-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="48a12-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="48a12-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="48a12-139">La routine inactive doit être désactivée lors de l'inscription.</span><span class="sxs-lookup"><span data-stu-id="48a12-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="48a12-140">L'action par défaut consiste à activer la routine inactive lorsque **FtgRegisterIdleRoutine** l'enregistre.</span><span class="sxs-lookup"><span data-stu-id="48a12-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="48a12-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="48a12-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="48a12-142">Le temps spécifié par le paramètre _csecIdle_ est l'intervalle minimal entre les appels successifs de la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="48a12-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="48a12-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="48a12-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="48a12-144">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="48a12-144">Obsolete.</span></span> <span data-ttu-id="48a12-145">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="48a12-145">Do not use.</span></span> 
      
  <span data-ttu-id="48a12-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="48a12-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="48a12-147">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="48a12-147">Obsolete.</span></span> <span data-ttu-id="48a12-148">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="48a12-148">Do not use.</span></span> 
      
  <span data-ttu-id="48a12-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="48a12-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="48a12-150">Le temps spécifié par le paramètre _csecIdle_ est la période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur d'inactivité MAPI appelle la routine inactive pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="48a12-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="48a12-151">Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="48a12-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48a12-152">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="48a12-152">Return value</span></span>

<span data-ttu-id="48a12-153">La fonction **FtgRegisterIdleRoutine** renvoie une balise de fonction identifiant la routine inactive qui a été ajoutée au système MAPI.</span><span class="sxs-lookup"><span data-stu-id="48a12-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="48a12-154">Si **FtgRegisterIdleRoutine** ne parvient pas à enregistrer la routine inactive pour l'application cliente ou le fournisseur de services, par exemple en raison de problèmes de mémoire, elle renvoie la valeur null.</span><span class="sxs-lookup"><span data-stu-id="48a12-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="48a12-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="48a12-155">Remarks</span></span>

<span data-ttu-id="48a12-156">Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="48a12-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="48a12-157">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="48a12-157">**Idle routine function**</span></span>|<span data-ttu-id="48a12-158">**Usage**</span><span class="sxs-lookup"><span data-stu-id="48a12-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48a12-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a12-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="48a12-160">Modifie les caractéristiques d'une routine inactive enregistrée.</span><span class="sxs-lookup"><span data-stu-id="48a12-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="48a12-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a12-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="48a12-162">Supprime une routine inactive inscrite du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="48a12-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="48a12-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="48a12-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="48a12-164">Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="48a12-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="48a12-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="48a12-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="48a12-166">Ajoute une routine inactive au système MAPI, avec ou sans l'activer.</span><span class="sxs-lookup"><span data-stu-id="48a12-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="48a12-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="48a12-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="48a12-168">Arrête le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="48a12-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="48a12-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="48a12-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="48a12-170">Initialise le moteur d'inactivité MAPI pour l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="48a12-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="48a12-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="48a12-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="48a12-172">Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="48a12-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="48a12-173">Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité.</span><span class="sxs-lookup"><span data-stu-id="48a12-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="48a12-174">Voici un exemple d'utilisation de l'indicateur FIRONOADJUSTMENT dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="48a12-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="48a12-175">Enregistrer une routine inactive avec un délai de 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="48a12-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="48a12-176">Mettre en veille/mettre l'ordinateur en veille après 1 minute (4 minutes restantes sur le minuteur).</span><span class="sxs-lookup"><span data-stu-id="48a12-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="48a12-177">Reprendre l'ordinateur 10 minutes plus tard.</span><span class="sxs-lookup"><span data-stu-id="48a12-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="48a12-178">Le comportement par défaut, sans FIRONOADJUSTMENT, est que vous devez attendre 4 minutes supplémentaires pour l'exécution de votre routine.</span><span class="sxs-lookup"><span data-stu-id="48a12-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="48a12-179">Autrement dit, votre minuteur a été ajusté pour permettre pendant combien de temps l'ordinateur était en mode veille.</span><span class="sxs-lookup"><span data-stu-id="48a12-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="48a12-180">Toutefois, si vous transmettez FIRONOADJUSTMENT, votre routine inactive s'exécutera immédiatement car plus de 5 minutes de temps réel se sont écoulées.</span><span class="sxs-lookup"><span data-stu-id="48a12-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

