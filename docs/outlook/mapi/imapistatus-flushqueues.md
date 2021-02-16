---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432603"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="e7e45-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e7e45-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="e7e45-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7e45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7e45-105">Force le téléchargement immédiat de tous les messages en attente d’envoi ou de réception.</span><span class="sxs-lookup"><span data-stu-id="e7e45-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="e7e45-106">L’objet d’état dupooler MAPI et les objets d’état implémentés par les fournisseurs de transport la prise en charge de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e7e45-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e7e45-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7e45-107">Parameters</span></span>

 <span data-ttu-id="e7e45-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e7e45-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="e7e45-109">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e7e45-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="e7e45-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="e7e45-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="e7e45-111">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpTargetTransport._</span><span class="sxs-lookup"><span data-stu-id="e7e45-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="e7e45-112">Le  _paramètre cbTargetTransport_ est uniquement définie sur les appels à l’objet d’état dupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7e45-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="e7e45-113">Pour les appels à un fournisseur de transport, le  _paramètre cbTargetTransport_ est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="e7e45-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="e7e45-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="e7e45-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="e7e45-115">[in] Pointeur vers l’identificateur d’entrée du fournisseur de transport qui doit vider ses files d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="e7e45-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="e7e45-116">Le  _paramètre lpTargetTransport_ est uniquement définie sur les appels à l’objet d’état dupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7e45-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="e7e45-117">Pour les appels à un fournisseur de transport,  _le paramètre lpTargetTransport_ est définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="e7e45-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="e7e45-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7e45-118">_ulFlags_</span></span>
  
> <span data-ttu-id="e7e45-119">[in] Masque de bits d’indicateurs qui contrôle l’opération de purge.</span><span class="sxs-lookup"><span data-stu-id="e7e45-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="e7e45-120">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="e7e45-120">The following flags can be set:</span></span>
    
<span data-ttu-id="e7e45-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="e7e45-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="e7e45-122">L’opération de purge peut se produire de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e7e45-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="e7e45-123">Cet indicateur s’applique uniquement à l’objet d’état dupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7e45-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="e7e45-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="e7e45-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="e7e45-125">Les files d’attente de messages entrants doivent être vidées.</span><span class="sxs-lookup"><span data-stu-id="e7e45-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="e7e45-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="e7e45-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="e7e45-127">L’opération de purge doit avoir lieu, malgré le risque de diminution des performances.</span><span class="sxs-lookup"><span data-stu-id="e7e45-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="e7e45-128">Cet indicateur doit être définie lorsqu’un fournisseur de transport asynchrone est ciblé.</span><span class="sxs-lookup"><span data-stu-id="e7e45-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="e7e45-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="e7e45-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="e7e45-130">L’objet d’état ne doit pas afficher d’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="e7e45-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="e7e45-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="e7e45-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="e7e45-132">Les files d’attente de messages sortantes doivent être vidées.</span><span class="sxs-lookup"><span data-stu-id="e7e45-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7e45-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e7e45-133">Return value</span></span>

<span data-ttu-id="e7e45-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7e45-134">S_OK</span></span> 
  
> <span data-ttu-id="e7e45-135">L’opération de purge a réussi.</span><span class="sxs-lookup"><span data-stu-id="e7e45-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="e7e45-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e7e45-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e7e45-137">Une autre opération est en cours ; Il doit être autorisé à se terminer, ou doit être arrêté, avant que cette opération puisse être lancée.</span><span class="sxs-lookup"><span data-stu-id="e7e45-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="e7e45-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e7e45-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e7e45-139">L’objet status ne prend pas en charge cette opération, comme indiqué par l’absence de l’indicateur STATUS_FLUSH_QUEUES dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="e7e45-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7e45-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7e45-140">Remarks</span></span>

<span data-ttu-id="e7e45-141">La méthode **IMAPIStatus::FlushQueues** demande aupooler MAPI ou à un fournisseur de transport d’envoyer immédiatement tous les messages de la file d’attente sortante ou de recevoir tous les messages de la file d’attente entrante.</span><span class="sxs-lookup"><span data-stu-id="e7e45-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="e7e45-142">**FlushQueues est** implémenté uniquement par l’objet d’état dupooler MAPI et par les objets d’état que les fournisseurs de transport fournissent.</span><span class="sxs-lookup"><span data-stu-id="e7e45-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="e7e45-143">MAPI_E_BUSY les demandes asynchrones doivent être renvoyées afin que les clients continuent à travailler.</span><span class="sxs-lookup"><span data-stu-id="e7e45-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="e7e45-144">Par défaut, **FlushQueues est** une opération synchrone ; ne revient pas à l’appelant tant que le purgement n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="e7e45-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="e7e45-145">Seule l’opération de purge effectuée par lepooler MAPI peut être asynchrone ; les clients demandent ce comportement en FLUSH_ASYNC_OK’indicateur.</span><span class="sxs-lookup"><span data-stu-id="e7e45-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e7e45-146">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e7e45-146">Notes to implementers</span></span>

<span data-ttu-id="e7e45-147">L’implémentation de **FlushQueues** par un fournisseur de transport distant définit des bits dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état de l’objet d’authentification pour contrôler la façon dont les files d’attente sont vidées.</span><span class="sxs-lookup"><span data-stu-id="e7e45-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="e7e45-148">Si une visionneuse distante passe dans l’indicateur FLUSH_UPLOAD, la méthode **FlushQueues** doit définir les STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE bits.</span><span class="sxs-lookup"><span data-stu-id="e7e45-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="e7e45-149">Si une visionneuse distante passe dans l’indicateur FLUSH_DOWNLOAD, la méthode **FlushQueues** doit définir les bits STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE distants.</span><span class="sxs-lookup"><span data-stu-id="e7e45-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="e7e45-150">**FlushQueues** doit ensuite renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="e7e45-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="e7e45-151">Lepooler MAPI lancera ensuite les actions appropriées pour charger et télécharger des messages.</span><span class="sxs-lookup"><span data-stu-id="e7e45-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e7e45-152">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e7e45-152">Notes to callers</span></span>

<span data-ttu-id="e7e45-153">Un appel à l’objet d’état dupooler MAPI est une directive qui consiste à transférer tous les messages vers ou depuis le fournisseur de transport approprié.</span><span class="sxs-lookup"><span data-stu-id="e7e45-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="e7e45-154">Lorsque vous appelez l’objet d’état d’un fournisseur de transport individuel, seuls les messages de ce fournisseur sont affectés.</span><span class="sxs-lookup"><span data-stu-id="e7e45-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7e45-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7e45-155">See also</span></span>



[<span data-ttu-id="e7e45-156">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="e7e45-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="e7e45-157">Propriété canonique PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="e7e45-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="e7e45-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e7e45-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

