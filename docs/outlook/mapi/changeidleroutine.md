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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 49682007946a4c5dda3800751deaebcc0e1e5740
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579451"
---
# <a name="changeidleroutine"></a><span data-ttu-id="57ed0-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="57ed0-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="57ed0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57ed0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57ed0-105">Modifie certaines ou toutes les caractéristiques d’une routine d’inactivité [FNIDLE](fnidle.md) en fonction de.</span><span class="sxs-lookup"><span data-stu-id="57ed0-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57ed0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="57ed0-106">Header file:</span></span>  <br/> |<span data-ttu-id="57ed0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="57ed0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="57ed0-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="57ed0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="57ed0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="57ed0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="57ed0-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="57ed0-110">Called by:</span></span>  <br/> |<span data-ttu-id="57ed0-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="57ed0-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="57ed0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57ed0-112">Parameters</span></span>

<span data-ttu-id="57ed0-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="57ed0-113">_ftg_</span></span>
  
> <span data-ttu-id="57ed0-114">[in] Balise de fonction qui identifie la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="57ed0-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="57ed0-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="57ed0-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="57ed0-116">[in] Pointeur vers la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="57ed0-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="57ed0-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="57ed0-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="57ed0-118">[in] Pointeur vers un nouveau bloc de mémoire qui alloue de l’implémentation d’appel de la routine d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="57ed0-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="57ed0-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="57ed0-119">_priIdle_</span></span>
  
> <span data-ttu-id="57ed0-120">[in] Valeur qui représente une nouvelle priorité de la routine d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="57ed0-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="57ed0-121">Priorités possibles pour les routines défini par l’implémentation sont supérieur ou inférieur à zéro, mais pas de zéro.</span><span class="sxs-lookup"><span data-stu-id="57ed0-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="57ed0-122">La valeur zéro est réservée pour un événement utilisateur comme un clic de souris ou d’un message WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="57ed0-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="57ed0-123">Les valeurs supérieures à zéro représentent des priorités pour les tâches en arrière-plan qui ont une priorité plus élevée que les événements de l’utilisateur et sont exécutés dans le cadre de la boucle de pompe de message Windows standard.</span><span class="sxs-lookup"><span data-stu-id="57ed0-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="57ed0-124">Les valeurs inférieures à zéro représentent des priorités pour les tâches inactives qui s’exécutent uniquement pendant les temps morts durant copie du message.</span><span class="sxs-lookup"><span data-stu-id="57ed0-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="57ed0-125">Exemples de priorités : 1 pour l’envoi de premier plan, 1 pour l’insertion de caractère power-modifier et 3 pour le téléchargement de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="57ed0-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="57ed0-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="57ed0-126">_csecIdle_</span></span>
  
> <span data-ttu-id="57ed0-127">[in] Une nouvelle date dans centième de seconde, à appliquer à la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="57ed0-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="57ed0-128">La signification de la valeur d’heure initiale varie, selon ce qui est passé dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="57ed0-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="57ed0-129">Il peut être :</span><span class="sxs-lookup"><span data-stu-id="57ed0-129">It can be:</span></span> 
    
  - <span data-ttu-id="57ed0-130">La durée minimale d’inaction utilisateur qui doit s’écouler avant l’interface MAPI moteur inactif appelle la routine inactive pour la première fois, si l’indicateur FIROWAIT est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="57ed0-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="57ed0-131">Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="57ed0-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="57ed0-132">L’intervalle minimal entre les appels à la routine inactive, si l’indicateur FIROINTERVAL est défini dans _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="57ed0-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="57ed0-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="57ed0-133">_iroIdle_</span></span>
  
> <span data-ttu-id="57ed0-134">[in] Masque de bits d’indicateurs indiquant les nouvelles options pour appeler la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="57ed0-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="57ed0-135">Un des indicateurs suivants doit être défini :</span><span class="sxs-lookup"><span data-stu-id="57ed0-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="57ed0-136">FIROINTERVAL : L’heure spécifiée par le paramètre _csecIdle_ est l’intervalle entre les appels successifs de la routine d’inactivité minimale.</span><span class="sxs-lookup"><span data-stu-id="57ed0-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="57ed0-137">FIROONCEONLY : obsolète.</span><span class="sxs-lookup"><span data-stu-id="57ed0-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="57ed0-138">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="57ed0-138">Do not use.</span></span> 
      
  - <span data-ttu-id="57ed0-139">FIROPERBLOCK : obsolète.</span><span class="sxs-lookup"><span data-stu-id="57ed0-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="57ed0-140">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="57ed0-140">Do not use.</span></span> 
      
  - <span data-ttu-id="57ed0-141">FIROWAIT : L’heure spécifiée par le paramètre _csecIdle_ est la durée minimale d’inaction utilisateur qui doit s’écouler avant que le moteur d’inactivité MAPI appelle la routine inactive pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="57ed0-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="57ed0-142">Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="57ed0-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="57ed0-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="57ed0-143">_ircIdle_</span></span>
  
> <span data-ttu-id="57ed0-144">[in] Masque de bits d’indicateurs utilisés pour indiquer les modifications à apporter à la routine inactive.</span><span class="sxs-lookup"><span data-stu-id="57ed0-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="57ed0-145">Les indicateurs suivants peuvent être définis dans n’importe quelle combinaison :</span><span class="sxs-lookup"><span data-stu-id="57ed0-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="57ed0-146">FIRCCSEC : Une modification apportée à l’heure associée à la routine inactive, c'est-à-dire, une modification indiquée par la valeur transmise au paramètre _csecIdle_ .</span><span class="sxs-lookup"><span data-stu-id="57ed0-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="57ed0-147">FIRCIRO : Une modification dans les options de la routine d’inactivité, autrement dit, une modification indiquée par la valeur passée dans le paramètre _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="57ed0-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="57ed0-148">FIRCPFN : Une modification du pointeur de routine inactif, autrement dit, une modification indiquée par la valeur passée dans le paramètre _pfnIdle_ .</span><span class="sxs-lookup"><span data-stu-id="57ed0-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="57ed0-149">FIRCPRI : Une modification apportée à la priorité de la routine d’inactivité, autrement dit, une modification indiquée par la valeur passée dans le paramètre _priIdle_ .</span><span class="sxs-lookup"><span data-stu-id="57ed0-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="57ed0-150">FIRCPV : Une modification dans le bloc de mémoire de la routine d’inactivité, autrement dit, une modification indiquée par la valeur passée dans le paramètre _pvIdleParam_ .</span><span class="sxs-lookup"><span data-stu-id="57ed0-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="57ed0-151">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57ed0-151">Return value</span></span>

<span data-ttu-id="57ed0-152">Aucun.</span><span class="sxs-lookup"><span data-stu-id="57ed0-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57ed0-153">Remarques</span><span class="sxs-lookup"><span data-stu-id="57ed0-153">Remarks</span></span>

<span data-ttu-id="57ed0-154">Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="57ed0-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="57ed0-155">**Fonction de routine inactive**</span><span class="sxs-lookup"><span data-stu-id="57ed0-155">**Idle routine function**</span></span>|<span data-ttu-id="57ed0-156">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="57ed0-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57ed0-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="57ed0-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="57ed0-158">Modifie les caractéristiques d’une routine d’inactivité inscrit.</span><span class="sxs-lookup"><span data-stu-id="57ed0-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="57ed0-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="57ed0-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="57ed0-160">Supprime une routine d’inactivité inscrit dans le système MAPI.</span><span class="sxs-lookup"><span data-stu-id="57ed0-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="57ed0-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="57ed0-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="57ed0-162">Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.</span><span class="sxs-lookup"><span data-stu-id="57ed0-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="57ed0-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="57ed0-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="57ed0-164">Ajoute une routine inactive au système MAPI, avec ou sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="57ed0-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="57ed0-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="57ed0-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="57ed0-166">Arrête le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="57ed0-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="57ed0-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="57ed0-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="57ed0-168">Initialise le moteur d’inactivité MAPI pour l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="57ed0-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="57ed0-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="57ed0-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="57ed0-170">Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter.</span><span class="sxs-lookup"><span data-stu-id="57ed0-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="57ed0-171">Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité.</span><span class="sxs-lookup"><span data-stu-id="57ed0-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

