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
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434017"
---
# <a name="notifcallback"></a><span data-ttu-id="bcd95-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="bcd95-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="bcd95-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcd95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcd95-105">Définit une fonction de rappel que MAPI appelle pour envoyer une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="bcd95-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="bcd95-106">Cette fonction de rappel peut uniquement être utilisée lorsqu’elle est wrapped dans un objet de sink de conseil créé en appelant la fonction [HrAllocAdviseSink.](hrallocadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="bcd95-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcd95-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bcd95-107">Header file:</span></span>  <br/> |<span data-ttu-id="bcd95-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcd95-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bcd95-109">Fonction définie implémentée par :</span><span class="sxs-lookup"><span data-stu-id="bcd95-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="bcd95-110">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bcd95-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="bcd95-111">Fonction définie appelée par :</span><span class="sxs-lookup"><span data-stu-id="bcd95-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="bcd95-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="bcd95-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="bcd95-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcd95-113">Parameters</span></span>

 <span data-ttu-id="bcd95-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="bcd95-114">_lpvContext_</span></span>
  
> <span data-ttu-id="bcd95-115">[in] Pointeur vers une valeur arbitraire transmise à la fonction de rappel lorsque MAPI l’appelle.</span><span class="sxs-lookup"><span data-stu-id="bcd95-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="bcd95-116">Cette valeur peut représenter une adresse significative pour l’application cliente ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="bcd95-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="bcd95-117">En règle générale, pour le code C++,  _le paramètre lpvContext_ représente un pointeur vers un objet C++.</span><span class="sxs-lookup"><span data-stu-id="bcd95-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="bcd95-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="bcd95-118">_cNotification_</span></span>
  
> <span data-ttu-id="bcd95-119">[in] Nombre de notifications d’événement dans le tableau indiqué par _le paramètre lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="bcd95-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="bcd95-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="bcd95-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="bcd95-121">[out] Pointeur vers l’emplacement où cette fonction écrit un tableau de structures [DE NOTIFICATION](notification.md) qui contient les notifications d’événement.</span><span class="sxs-lookup"><span data-stu-id="bcd95-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bcd95-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bcd95-122">Return value</span></span>

<span data-ttu-id="bcd95-123">L’ensemble des valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** varie selon que la fonction est implémentée par une application cliente ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="bcd95-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="bcd95-124">Les clients doivent toujours renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="bcd95-124">Clients should always return S_OK.</span></span> <span data-ttu-id="bcd95-125">Les fournisseurs peuvent renvoyer S_OK ou CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="bcd95-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bcd95-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="bcd95-126">Remarks</span></span>

<span data-ttu-id="bcd95-127">CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrones uniquement ; Il demande à MAPI d’arrêter immédiatement le traitement des rappels pour cette notification.</span><span class="sxs-lookup"><span data-stu-id="bcd95-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="bcd95-128">Lorsque CALLBACK_DISCONTINUE est renvoyé, MAPI définit le paramètre  _lpUlFlags_ sur NOTIFY_CANCELED lorsqu’il revient à partir [d’IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="bcd95-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="bcd95-129">Les limitations suivantes limitent ce que peut faire une fonction de rappel synchrone :</span><span class="sxs-lookup"><span data-stu-id="bcd95-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="bcd95-130">Il ne peut pas générer une autre notification synchrone.</span><span class="sxs-lookup"><span data-stu-id="bcd95-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="bcd95-131">Il ne peut pas afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bcd95-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcd95-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcd95-132">See also</span></span>



[<span data-ttu-id="bcd95-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bcd95-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

