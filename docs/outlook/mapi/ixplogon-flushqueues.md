---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 961ac2d26cd58e625c35d00bd1216cdee2ce57a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584729"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="31bad-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="31bad-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="31bad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31bad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31bad-105">Demande que le fournisseur de transport remettre immédiatement tous les messages entrants ou sortants en attente.</span><span class="sxs-lookup"><span data-stu-id="31bad-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="31bad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31bad-106">Parameters</span></span>

 <span data-ttu-id="31bad-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="31bad-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="31bad-108">[in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.</span><span class="sxs-lookup"><span data-stu-id="31bad-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="31bad-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="31bad-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="31bad-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="31bad-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="31bad-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="31bad-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="31bad-112">[in] Réservé ; doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="31bad-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="31bad-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31bad-113">_ulFlags_</span></span>
  
> <span data-ttu-id="31bad-114">[in] Masque de bits d’indicateurs qui contrôle comment la purge des messages en file d’attente est effectué.</span><span class="sxs-lookup"><span data-stu-id="31bad-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="31bad-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="31bad-115">The following flags can be set:</span></span>
    
<span data-ttu-id="31bad-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="31bad-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="31bad-117">La file d’attente de messages entrants ou les files d’attente doivent être vidés.</span><span class="sxs-lookup"><span data-stu-id="31bad-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="31bad-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="31bad-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="31bad-119">Le fournisseur de transport doit traiter cette demande, si possible, même si cela n’est beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="31bad-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="31bad-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="31bad-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="31bad-121">Le fournisseur de transport ne doit pas afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31bad-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="31bad-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="31bad-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="31bad-123">La file d’attente de messages sortants ou les files d’attente doivent être vidés.</span><span class="sxs-lookup"><span data-stu-id="31bad-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31bad-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="31bad-124">Return value</span></span>

<span data-ttu-id="31bad-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="31bad-125">S_OK</span></span> 
  
> <span data-ttu-id="31bad-126">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="31bad-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31bad-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="31bad-127">Remarks</span></span>

<span data-ttu-id="31bad-128">Le spouleur MAPI appelle la méthode **IXPLogon::FlushQueues** pour conseiller le fournisseur de transport que le spouleur MAPI est sur le point de commencer le traitement des messages.</span><span class="sxs-lookup"><span data-stu-id="31bad-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="31bad-129">Le fournisseur de transport doit appeler la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour définir un bit approprié pour son état dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état.</span><span class="sxs-lookup"><span data-stu-id="31bad-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="31bad-130">Après la mise à jour de la ligne d’état, le fournisseur de transport doit renvoyer S_OK pour l’appel de **FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="31bad-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="31bad-131">Le spouleur MAPI démarre ensuite l’envoi des messages, l’opération en cours synchrone pour le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="31bad-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="31bad-132">Pour prendre en charge son implémentation de la méthode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , le spouleur MAPI appelle **IXPLogon::FlushQueues** pour tous les objets d’ouverture de session pour les fournisseurs de transport actif qui sont en cours d’exécution dans une session de profil.</span><span class="sxs-lookup"><span data-stu-id="31bad-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="31bad-133">Lorsque la méthode de **FlushQueues** d’un fournisseur de transport est appelée à la suite d’une application cliente appelle à **IMAPIStatus::FlushQueues**, le traitement du message se produit en mode asynchrone au client.</span><span class="sxs-lookup"><span data-stu-id="31bad-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31bad-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31bad-134">See also</span></span>



[<span data-ttu-id="31bad-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="31bad-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="31bad-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31bad-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

