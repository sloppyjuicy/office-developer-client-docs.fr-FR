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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783385"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="01cea-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01cea-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="01cea-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01cea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01cea-105">Ajoute une routine [FNIDLE](fnidle.md) fonction inactive au système MAPI.</span><span class="sxs-lookup"><span data-stu-id="01cea-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01cea-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="01cea-106">Header file:</span></span>  <br/> |<span data-ttu-id="01cea-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="01cea-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01cea-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="01cea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01cea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01cea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01cea-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="01cea-110">Called by:</span></span>  <br/> |<span data-ttu-id="01cea-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="01cea-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="01cea-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01cea-112">Parameters</span></span>

<span data-ttu-id="01cea-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="01cea-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="01cea-114">[in] Pointeur vers la routine inactif.</span><span class="sxs-lookup"><span data-stu-id="01cea-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="01cea-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="01cea-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="01cea-116">[in] Pointeur vers un bloc de mémoire que le moteur d’inactivité doit transmettre en tant que paramètre à la routine inactive lorsqu’il l’appelle.</span><span class="sxs-lookup"><span data-stu-id="01cea-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="01cea-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="01cea-117">_priIdle_</span></span>
  
> <span data-ttu-id="01cea-118">[in] La priorité initiale de la routine d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="01cea-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="01cea-119">Priorités possibles pour les routines défini par l’implémentation sont supérieur ou inférieur à zéro, mais pas de zéro.</span><span class="sxs-lookup"><span data-stu-id="01cea-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="01cea-120">La priorité de zéro est réservée pour un événement utilisateur comme un clic de souris ou d’un message WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="01cea-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="01cea-121">Supérieure à zéro des priorités représentent des tâches en arrière-plan qui ont une priorité plus élevée que les événements de l’utilisateur et sont exécutés dans le cadre de la boucle de pompe de message Windows standard.</span><span class="sxs-lookup"><span data-stu-id="01cea-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="01cea-122">Priorités inférieur à zéro représente les tâches inactives uniquement être exécutées pendant la durée d’inactivité pompe message.</span><span class="sxs-lookup"><span data-stu-id="01cea-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="01cea-123">Exemples de priorités sont les suivantes : 1 pour l’envoi de premier plan, 2 pour l’insertion de caractère power-modifier et 3 pour le téléchargement de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="01cea-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="01cea-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="01cea-124">_csecIdle_</span></span>
  
> <span data-ttu-id="01cea-125">[in] La valeur de la première fois, dans centième de seconde, à utiliser pour spécifier les paramètres de routine inactifs.</span><span class="sxs-lookup"><span data-stu-id="01cea-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="01cea-126">La signification de la valeur d’heure initiale varie, selon ce qui est passé dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="01cea-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="01cea-127">La signification peut être une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="01cea-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="01cea-128">La durée minimale d’inaction utilisateur qui doit s’écouler avant l’interface MAPI moteur inactif appelle la routine inactive pour la première fois, si l’indicateur FIROWAIT est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="01cea-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="01cea-129">Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="01cea-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="01cea-130">L’intervalle minimal entre les appels à la routine inactive, si l’indicateur FIROINTERVAL est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="01cea-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="01cea-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="01cea-131">_iroIdle_</span></span>
  
> <span data-ttu-id="01cea-132">[in] Masque de bits d’indicateurs utilisés pour définir les options initiales de la routine d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="01cea-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="01cea-133">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="01cea-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="01cea-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="01cea-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="01cea-135">Utilisez cet indicateur pour spécifier que l’horloge de routine ne doit pas être ajustée pour la mise en veille ou de reprendre.</span><span class="sxs-lookup"><span data-stu-id="01cea-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="01cea-136">Le comportement par défaut sans cet indicateur est que la durée de veille est exclue lors du calcul du temps écoulé.</span><span class="sxs-lookup"><span data-stu-id="01cea-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="01cea-137">Si FIRONOADJUSTMENT est passée la durée de veille est incluse lors du calcul de temps écoulé.</span><span class="sxs-lookup"><span data-stu-id="01cea-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="01cea-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="01cea-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="01cea-139">La routine d’inactivité doit être désactivée lorsque enregistré.</span><span class="sxs-lookup"><span data-stu-id="01cea-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="01cea-140">L’action par défaut consiste à activer la routine inactive lorsque **FtgRegisterIdleRoutine** inscrit.</span><span class="sxs-lookup"><span data-stu-id="01cea-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="01cea-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="01cea-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="01cea-142">L’heure spécifiée par le paramètre _csecIdle_ est l’intervalle entre les appels successifs de la routine d’inactivité minimale.</span><span class="sxs-lookup"><span data-stu-id="01cea-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="01cea-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="01cea-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="01cea-p107">Obsolète. Ne pas utiliser. </span><span class="sxs-lookup"><span data-stu-id="01cea-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="01cea-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="01cea-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="01cea-p108">Obsolète. Ne pas utiliser. </span><span class="sxs-lookup"><span data-stu-id="01cea-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="01cea-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="01cea-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="01cea-150">L’heure spécifiée par le paramètre _csecIdle_ est la durée minimale d’inaction utilisateur qui doit s’écouler avant que le moteur d’inactivité MAPI appelle la routine inactive pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="01cea-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="01cea-151">Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="01cea-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="01cea-152">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="01cea-152">Return value</span></span>

<span data-ttu-id="01cea-153">La fonction **FtgRegisterIdleRoutine** renvoie une balise de fonction qui identifie la routine d’inactivité qui a été ajoutée au système MAPI.</span><span class="sxs-lookup"><span data-stu-id="01cea-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="01cea-154">Si **FtgRegisterIdleRoutine** ne peut pas enregistrer la routine d’inactivité pour l’application cliente ou d’un fournisseur de services, par exemple en raison de problèmes de mémoire, elle renvoie la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="01cea-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="01cea-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="01cea-155">Remarks</span></span>

<span data-ttu-id="01cea-156">Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="01cea-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="01cea-157">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="01cea-157">**Idle routine function**</span></span>|<span data-ttu-id="01cea-158">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="01cea-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01cea-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01cea-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="01cea-160">Modifie les caractéristiques d’une routine d’inactivité inscrit.</span><span class="sxs-lookup"><span data-stu-id="01cea-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="01cea-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01cea-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="01cea-162">Supprime une routine d’inactivité inscrit dans le système MAPI.</span><span class="sxs-lookup"><span data-stu-id="01cea-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="01cea-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01cea-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="01cea-164">Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="01cea-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="01cea-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="01cea-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="01cea-166">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="01cea-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="01cea-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="01cea-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="01cea-168">Arrête le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="01cea-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="01cea-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="01cea-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="01cea-170">Initialise le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="01cea-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="01cea-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="01cea-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="01cea-172">Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="01cea-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="01cea-173">Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité.</span><span class="sxs-lookup"><span data-stu-id="01cea-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="01cea-174">Voici un exemple d’utilisation de l’indicateur FIRONOADJUSTMENT dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="01cea-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="01cea-175">Enregistrer une routine inactive avec un délai de 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="01cea-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="01cea-176">Mise en veille prolongée/veille l’ordinateur après 1 minute (4 minutes à gauche de l’horloge).</span><span class="sxs-lookup"><span data-stu-id="01cea-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="01cea-177">Redémarrez l’ordinateur 10 minutes plus tard.</span><span class="sxs-lookup"><span data-stu-id="01cea-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="01cea-178">Le comportement par défaut, sans FIRONOADJUSTMENT, est que vous devrez attendre 4 minutes pour exécuter votre routine.</span><span class="sxs-lookup"><span data-stu-id="01cea-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="01cea-179">Autrement dit, le minuteur a été ajustée pour permettre la durée pendant laquelle l’ordinateur était en veille.</span><span class="sxs-lookup"><span data-stu-id="01cea-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="01cea-180">Toutefois, si vous transmettez FIRONOADJUSTMENT votre routine inactif exécutera immédiatement car plus de 5 minutes de temps réel se sont écoulées.</span><span class="sxs-lookup"><span data-stu-id="01cea-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

