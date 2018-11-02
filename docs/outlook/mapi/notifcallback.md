---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 17b038fea2dd1614f94f005e32b9e6ba4423dbda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566263"
---
# <a name="notifcallback"></a><span data-ttu-id="5abf2-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="5abf2-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="5abf2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5abf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5abf2-105">Définit une fonction de rappel appels MAPI pour envoyer une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="5abf2-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="5abf2-106">Cette fonction de rappel peut être utilisée uniquement lorsqu’encapsulé dans un objet de récepteur advise créé en appelant la fonction [HrAllocAdviseSink](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="5abf2-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5abf2-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5abf2-107">Header file:</span></span>  <br/> |<span data-ttu-id="5abf2-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5abf2-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5abf2-109">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="5abf2-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5abf2-110">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5abf2-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="5abf2-111">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="5abf2-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5abf2-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="5abf2-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="5abf2-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5abf2-113">Parameters</span></span>

 <span data-ttu-id="5abf2-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="5abf2-114">_lpvContext_</span></span>
  
> <span data-ttu-id="5abf2-115">[in] Pointeur vers une valeur arbitraire transmis à la fonction de rappel lorsque MAPI il l’appelle.</span><span class="sxs-lookup"><span data-stu-id="5abf2-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="5abf2-116">Cette valeur peut représenter une adresse de l’argument précision pour l’application cliente ou d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="5abf2-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="5abf2-117">En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers un objet C++.</span><span class="sxs-lookup"><span data-stu-id="5abf2-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="5abf2-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="5abf2-118">_cNotification_</span></span>
  
> <span data-ttu-id="5abf2-119">[in] Nombre de notifications d’événements dans le tableau indiqué par le paramètre _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="5abf2-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="5abf2-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="5abf2-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="5abf2-121">[out] Pointeur vers l’emplacement où cette fonction écrit un tableau de structures [NOTIFICATION](notification.md) qui contient les notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="5abf2-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5abf2-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5abf2-122">Return value</span></span>

<span data-ttu-id="5abf2-123">L’ensemble de valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** dépend si la fonction est implémentée par une application cliente ou d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="5abf2-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="5abf2-124">Les clients doivent toujours retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="5abf2-124">Clients should always return S_OK.</span></span> <span data-ttu-id="5abf2-125">Fournisseurs peuvent renvoyer S_OK ou CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="5abf2-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5abf2-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="5abf2-126">Remarks</span></span>

<span data-ttu-id="5abf2-127">CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrone uniquement ; il demande que MAPI arrêter immédiatement traitement des rappels pour cette notification.</span><span class="sxs-lookup"><span data-stu-id="5abf2-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="5abf2-128">Lorsque CALLBACK_DISCONTINUE est renvoyée, MAPI attribue au paramètre _lpUlFlags_ NOTIFY_CANCELED lorsqu’il retourne de [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="5abf2-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="5abf2-129">Limitations sur ce que peut faire une fonction de rappel synchrone sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5abf2-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="5abf2-130">Il ne peut pas provoquer la génération d’une autre notification synchrone.</span><span class="sxs-lookup"><span data-stu-id="5abf2-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="5abf2-131">Il ne peut pas afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5abf2-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5abf2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5abf2-132">See also</span></span>



[<span data-ttu-id="5abf2-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5abf2-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

