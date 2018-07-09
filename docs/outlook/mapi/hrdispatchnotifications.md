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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 28afa338b37e747ed441a8767981b7e63808e741
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783541"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="d7f66-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="d7f66-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="d7f66-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7f66-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7f66-105">Répartition des forces de toutes les notifications en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d7f66-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7f66-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d7f66-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7f66-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d7f66-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d7f66-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="d7f66-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7f66-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7f66-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7f66-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="d7f66-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7f66-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d7f66-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d7f66-112">Param�tres</span><span class="sxs-lookup"><span data-stu-id="d7f66-112">Parameters</span></span>

 <span data-ttu-id="d7f66-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7f66-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d7f66-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="d7f66-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7f66-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d7f66-115">Return value</span></span>

<span data-ttu-id="d7f66-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7f66-116">S_OK</span></span>
  
> <span data-ttu-id="d7f66-117">Toutes les notifications en file d’attente ont été acheminées.</span><span class="sxs-lookup"><span data-stu-id="d7f66-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="d7f66-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d7f66-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="d7f66-119">WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION a été reçue.</span><span class="sxs-lookup"><span data-stu-id="d7f66-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="d7f66-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="d7f66-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="d7f66-121">MAPI n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="d7f66-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7f66-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7f66-122">Remarks</span></span>

<span data-ttu-id="d7f66-123">La fonction **HrDispatchNotifications** entraîne MAPI distribuer toutes les notifications sont actuellement en file d’attente dans le moteur de notification MAPI sans attendre une intervention du message.</span><span class="sxs-lookup"><span data-stu-id="d7f66-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="d7f66-124">Cela peut avoir un effet bénéfique sur l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d7f66-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="d7f66-125">Pour plus d’informations, voir [forcer une Notification](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="d7f66-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d7f66-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="d7f66-126">Notes to callers</span></span>

<span data-ttu-id="d7f66-127">Certaines applications attendent un message de notification dans une boucle de délai d’expiration en utilisant les fonctions [DispatchMessage](http://msdn.microsoft.com/fr-fr/library/ms644934.aspx) Windows [PeekMessage](http://msdn.microsoft.com/fr-fr/library/ms644943.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d7f66-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/fr-fr/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/fr-fr/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="d7f66-128">Sur tous les, mais les plateformes plus rapides, ces applications peuvent rencontrer des performances médiocres ou même blocage de notifications.</span><span class="sxs-lookup"><span data-stu-id="d7f66-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="d7f66-129">À l’aide de **HrDispatchNotifications** non seulement réduit code mais améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="d7f66-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

