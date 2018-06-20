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
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784910"
---
# <a name="notifcallback"></a><span data-ttu-id="bbb1b-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="bbb1b-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="bbb1b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbb1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbb1b-105">Définit une fonction de rappel appels MAPI pour envoyer une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="bbb1b-106">Cette fonction de rappel peut être utilisée uniquement lorsqu’encapsulé dans un objet de récepteur advise créé en appelant la fonction [HrAllocAdviseSink](hrallocadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb1b-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbb1b-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bbb1b-107">Header file:</span></span>  <br/> |<span data-ttu-id="bbb1b-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbb1b-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bbb1b-109">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="bbb1b-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="bbb1b-110">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bbb1b-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="bbb1b-111">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="bbb1b-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="bbb1b-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="bbb1b-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="bbb1b-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbb1b-113">Parameters</span></span>

 <span data-ttu-id="bbb1b-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="bbb1b-114">_lpvContext_</span></span>
  
> <span data-ttu-id="bbb1b-115">[in] Pointeur vers une valeur arbitraire transmis à la fonction de rappel lorsque MAPI il l’appelle.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="bbb1b-116">Cette valeur peut représenter une adresse de l’argument précision pour l’application cliente ou d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="bbb1b-117">En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers un objet C++.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="bbb1b-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="bbb1b-118">_cNotification_</span></span>
  
> <span data-ttu-id="bbb1b-119">[in] Nombre de notifications d’événements dans le tableau indiqué par le paramètre _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="bbb1b-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="bbb1b-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="bbb1b-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="bbb1b-121">[out] Pointeur vers l’emplacement où cette fonction écrit un tableau de structures [NOTIFICATION](notification.md) qui contient les notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bbb1b-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bbb1b-122">Return value</span></span>

<span data-ttu-id="bbb1b-123">L’ensemble de valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** dépend si la fonction est implémentée par une application cliente ou d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="bbb1b-124">Les clients doivent toujours retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-124">Clients should always return S_OK.</span></span> <span data-ttu-id="bbb1b-125">Fournisseurs peuvent renvoyer S_OK ou CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bbb1b-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="bbb1b-126">Remarks</span></span>

<span data-ttu-id="bbb1b-127">CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrone uniquement ; il demande que MAPI arrêter immédiatement traitement des rappels pour cette notification.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="bbb1b-128">Lorsque CALLBACK_DISCONTINUE est renvoyée, MAPI attribue au paramètre _lpUlFlags_ NOTIFY_CANCELED lorsqu’il retourne de [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="bbb1b-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="bbb1b-129">Limitations sur ce que peut faire une fonction de rappel synchrone sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bbb1b-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="bbb1b-130">Il ne peut pas provoquer la génération d’une autre notification synchrone.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="bbb1b-131">Il ne peut pas afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bbb1b-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbb1b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbb1b-132">See also</span></span>



[<span data-ttu-id="bbb1b-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bbb1b-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

