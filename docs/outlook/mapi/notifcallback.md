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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334474"
---
# <a name="notifcallback"></a><span data-ttu-id="48bd6-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="48bd6-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="48bd6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48bd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48bd6-105">Définit une fonction de rappel que MAPI appelle pour envoyer une notification d'événement.</span><span class="sxs-lookup"><span data-stu-id="48bd6-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="48bd6-106">Cette fonction de rappel ne peut être utilisée que lorsqu'elle est incluse dans un wrapper dans un objet de récepteur de notifications créé en appelant la fonction [HrAllocAdviseSink](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="48bd6-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48bd6-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="48bd6-107">Header file:</span></span>  <br/> |<span data-ttu-id="48bd6-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="48bd6-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="48bd6-109">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="48bd6-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="48bd6-110">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="48bd6-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="48bd6-111">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="48bd6-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="48bd6-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="48bd6-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="48bd6-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48bd6-113">Parameters</span></span>

 <span data-ttu-id="48bd6-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="48bd6-114">_lpvContext_</span></span>
  
> <span data-ttu-id="48bd6-115">dans Pointeur vers une valeur arbitraire passée à la fonction de rappel lorsque MAPI l'appelle.</span><span class="sxs-lookup"><span data-stu-id="48bd6-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="48bd6-116">Cette valeur peut représenter une adresse de signification pour l'application cliente ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="48bd6-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="48bd6-117">En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers un objet c++.</span><span class="sxs-lookup"><span data-stu-id="48bd6-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="48bd6-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="48bd6-118">_cNotification_</span></span>
  
> <span data-ttu-id="48bd6-119">dans Nombre de notifications d'événement dans le tableau indiqué par le paramètre _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="48bd6-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="48bd6-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="48bd6-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="48bd6-121">remarquer Pointeur vers l'emplacement où cette fonction écrit un tableau de structures de [notification](notification.md) qui contient les notifications d'événement.</span><span class="sxs-lookup"><span data-stu-id="48bd6-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48bd6-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="48bd6-122">Return value</span></span>

<span data-ttu-id="48bd6-123">L'ensemble des valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** varie selon que la fonction est implémentée par une application cliente ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="48bd6-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="48bd6-124">Les clients doivent toujours retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="48bd6-124">Clients should always return S_OK.</span></span> <span data-ttu-id="48bd6-125">Les fournisseurs peuvent retourner S_OK ou CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="48bd6-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="48bd6-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="48bd6-126">Remarks</span></span>

<span data-ttu-id="48bd6-127">CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrone uniquement; Il demande que l'interface MAPI cesse immédiatement de traiter les rappels pour cette notification.</span><span class="sxs-lookup"><span data-stu-id="48bd6-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="48bd6-128">Lorsque CALLBACK_DISCONTINUE est renvoyé, MAPI définit le paramètre _lpUlFlags_ sur NOTIFY_CANCELED lorsqu'il revient de [IMAPISupport:: Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="48bd6-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="48bd6-129">Les éléments suivants sont des limitations de ce qu'une fonction de rappel synchrone peut effectuer:</span><span class="sxs-lookup"><span data-stu-id="48bd6-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="48bd6-130">Il ne peut pas provoquer la génération d'une autre notification synchrone.</span><span class="sxs-lookup"><span data-stu-id="48bd6-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="48bd6-131">Il ne peut pas afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48bd6-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48bd6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48bd6-132">See also</span></span>



[<span data-ttu-id="48bd6-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="48bd6-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

