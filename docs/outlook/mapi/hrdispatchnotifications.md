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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348096"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="bbaab-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="bbaab-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="bbaab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbaab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbaab-105">Force la distribution de toutes les notifications en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="bbaab-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbaab-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bbaab-106">Header file:</span></span>  <br/> |<span data-ttu-id="bbaab-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bbaab-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bbaab-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bbaab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bbaab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bbaab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bbaab-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bbaab-110">Called by:</span></span>  <br/> |<span data-ttu-id="bbaab-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bbaab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bbaab-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="bbaab-112">Parameters</span></span>

 <span data-ttu-id="bbaab-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbaab-113">_ulFlags_</span></span>
  
> <span data-ttu-id="bbaab-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="bbaab-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bbaab-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bbaab-115">Return value</span></span>

<span data-ttu-id="bbaab-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbaab-116">S_OK</span></span>
  
> <span data-ttu-id="bbaab-117">Toutes les notifications en file d’attente ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="bbaab-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="bbaab-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="bbaab-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="bbaab-119">WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION reçu.</span><span class="sxs-lookup"><span data-stu-id="bbaab-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="bbaab-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="bbaab-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="bbaab-121">MAPI n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="bbaab-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbaab-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="bbaab-122">Remarks</span></span>

<span data-ttu-id="bbaab-123">La **fonction HrDispatchNotifications** fait en sorte que MAPI envoie toutes les notifications actuellement en file d’attente dans le moteur de notification MAPI sans attendre une distribution de message.</span><span class="sxs-lookup"><span data-stu-id="bbaab-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="bbaab-124">Cela peut avoir un effet bénéfique sur l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="bbaab-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="bbaab-125">Pour plus d’informations, voir [Forcer une notification.](forcing-a-notification.md)</span><span class="sxs-lookup"><span data-stu-id="bbaab-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbaab-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="bbaab-126">Notes to callers</span></span>

<span data-ttu-id="bbaab-127">Certaines applications attendent un message de notification dans une boucle de délai d’attente à l’aide Windows [fonctions PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) et [DispatchMessage.](https://msdn.microsoft.com/library/ms644934.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbaab-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="bbaab-128">Sur toutes les plateformes, sauf sur les plateformes les plus rapides, ces applications peuvent faire l’expérience de performances médiocres ou même d’un blocage des notifications.</span><span class="sxs-lookup"><span data-stu-id="bbaab-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="bbaab-129">**L’utilisation de HrDispatchNotifications réduit** non seulement le code, mais améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="bbaab-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

