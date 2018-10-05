---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385563"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="27e6f-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="27e6f-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="27e6f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27e6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27e6f-105">Répartition des forces de toutes les notifications en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="27e6f-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27e6f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="27e6f-106">Header file:</span></span>  <br/> |<span data-ttu-id="27e6f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="27e6f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="27e6f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="27e6f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="27e6f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="27e6f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="27e6f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="27e6f-110">Called by:</span></span>  <br/> |<span data-ttu-id="27e6f-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="27e6f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="27e6f-112">Param�tres</span><span class="sxs-lookup"><span data-stu-id="27e6f-112">Parameters</span></span>

 <span data-ttu-id="27e6f-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27e6f-113">_ulFlags_</span></span>
  
> <span data-ttu-id="27e6f-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="27e6f-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27e6f-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27e6f-115">Return value</span></span>

<span data-ttu-id="27e6f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="27e6f-116">S_OK</span></span>
  
> <span data-ttu-id="27e6f-117">Toutes les notifications en file d’attente ont été acheminées.</span><span class="sxs-lookup"><span data-stu-id="27e6f-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="27e6f-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="27e6f-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="27e6f-119">WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION a été reçue.</span><span class="sxs-lookup"><span data-stu-id="27e6f-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="27e6f-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="27e6f-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="27e6f-121">MAPI n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="27e6f-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27e6f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="27e6f-122">Remarks</span></span>

<span data-ttu-id="27e6f-123">La fonction **HrDispatchNotifications** entraîne MAPI distribuer toutes les notifications sont actuellement en file d’attente dans le moteur de notification MAPI sans attendre une intervention du message.</span><span class="sxs-lookup"><span data-stu-id="27e6f-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="27e6f-124">Cela peut avoir un effet bénéfique sur l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="27e6f-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="27e6f-125">Pour plus d’informations, voir [forcer une Notification](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="27e6f-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="27e6f-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="27e6f-126">Notes to callers</span></span>

<span data-ttu-id="27e6f-127">Certaines applications attendent un message de notification dans une boucle de délai d’expiration en utilisant les fonctions [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27e6f-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="27e6f-128">Sur tous les, mais les plateformes plus rapides, ces applications peuvent rencontrer des performances médiocres ou même blocage de notifications.</span><span class="sxs-lookup"><span data-stu-id="27e6f-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="27e6f-129">À l’aide de **HrDispatchNotifications** non seulement réduit code mais améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="27e6f-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

