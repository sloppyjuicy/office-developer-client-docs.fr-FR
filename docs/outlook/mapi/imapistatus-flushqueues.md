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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d6c221ae307edb9d84cfcc0026660ea4bce7fadd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783959"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="a6458-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a6458-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="a6458-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6458-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6458-105">Force tous les messages en attente d’être envoyés ou reçus pour être immédiatement téléchargé ou téléchargé.</span><span class="sxs-lookup"><span data-stu-id="a6458-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="a6458-106">Les objets de statut qui implémentent des fournisseurs de transport et de l’objet état spouleur MAPI prennent en charge cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a6458-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a6458-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6458-107">Parameters</span></span>

 <span data-ttu-id="a6458-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a6458-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="a6458-109">[in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a6458-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a6458-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="a6458-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="a6458-111">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpTargetTransport_ .</span><span class="sxs-lookup"><span data-stu-id="a6458-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="a6458-112">Le paramètre _cbTargetTransport_ est défini uniquement sur les appels à l’objet d’état du spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="a6458-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="a6458-113">Pour les appels à un fournisseur de transport, le paramètre _cbTargetTransport_ est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="a6458-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="a6458-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="a6458-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="a6458-115">[in] Pointeur vers l’identificateur d’entrée du fournisseur de transport consiste à vider les files d’attente.</span><span class="sxs-lookup"><span data-stu-id="a6458-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="a6458-116">Le paramètre _lpTargetTransport_ est défini uniquement sur les appels à l’objet d’état du spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="a6458-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="a6458-117">Pour les appels à un fournisseur de transport, le paramètre _lpTargetTransport_ est défini sur NULL.</span><span class="sxs-lookup"><span data-stu-id="a6458-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="a6458-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6458-118">_ulFlags_</span></span>
  
> <span data-ttu-id="a6458-119">[in] Masque de bits d’indicateurs qui contrôle l’opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="a6458-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="a6458-120">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="a6458-120">The following flags can be set:</span></span>
    
<span data-ttu-id="a6458-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="a6458-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="a6458-122">L’opération de vidage peut se produire de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a6458-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="a6458-123">Cet indicateur s’applique uniquement à l’objet d’état du spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="a6458-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="a6458-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="a6458-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="a6458-125">Les files d’attente de messages entrants doivent être vidés.</span><span class="sxs-lookup"><span data-stu-id="a6458-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="a6458-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="a6458-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="a6458-127">L’opération de vidage doit se produire malgré tout, malgré le risque d’une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="a6458-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="a6458-128">Cet indicateur doit être défini lors de la cible d’un fournisseur de transport asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a6458-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="a6458-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="a6458-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="a6458-130">L’objet de l’état ne doit pas afficher un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="a6458-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="a6458-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="a6458-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="a6458-132">Les files d’attente de messages sortants doivent être vidés.</span><span class="sxs-lookup"><span data-stu-id="a6458-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6458-133">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a6458-133">Return value</span></span>

<span data-ttu-id="a6458-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6458-134">S_OK</span></span> 
  
> <span data-ttu-id="a6458-135">L’opération de vidage a réussi.</span><span class="sxs-lookup"><span data-stu-id="a6458-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="a6458-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a6458-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a6458-137">Une autre opération est en cours ; Il doit être autorisé pour effectuer, ou il doit être arrêté, avant cette opération peut être lancée.</span><span class="sxs-lookup"><span data-stu-id="a6458-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="a6458-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a6458-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a6458-139">L’objet état ne gère pas cette opération, comme indiqué par l’absence de l’indicateur STATUS_FLUSH_QUEUES dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="a6458-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6458-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6458-140">Remarks</span></span>

<span data-ttu-id="a6458-141">La méthode **IMAPIStatus::FlushQueues** demande le spouleur MAPI ou un fournisseur de transport immédiatement envoyer tous les messages dans la file d’attente sortante ou reçoivent tous les messages à partir de la file d’attente entrant.</span><span class="sxs-lookup"><span data-stu-id="a6458-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="a6458-142">**FlushQueues** est implémentée uniquement par l’objet d’état spouleur MAPI et par les objets d’état qui offre des fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="a6458-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="a6458-143">MAPI_E_BUSY doit être retournée pour les demandes asynchrones afin que les clients peuvent continuer de travail.</span><span class="sxs-lookup"><span data-stu-id="a6458-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="a6458-144">Par défaut, **FlushQueues** est une opération synchrone ; contrôle ne retourne pas à l’appelant jusqu'à ce que le vidage est terminée.</span><span class="sxs-lookup"><span data-stu-id="a6458-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="a6458-145">Uniquement l’opération de vidage effectuée par le spouleur MAPI peut être asynchrone ; les clients demandent ce comportement en définissant l’indicateur FLUSH_ASYNC_OK.</span><span class="sxs-lookup"><span data-stu-id="a6458-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6458-146">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a6458-146">Notes to implementers</span></span>

<span data-ttu-id="a6458-147">Implémentation d’un fournisseur de transport à distance de **FlushQueues** définit des bits dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) dans la ligne d’état de l’objet d’ouverture de session pour contrôler la façon dont les files d’attente sont vidés.</span><span class="sxs-lookup"><span data-stu-id="a6458-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="a6458-148">Si l’indicateur FLUSH_UPLOAD passe une visionneuse à distance, la méthode **FlushQueues** doit définir les bits STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="a6458-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="a6458-149">Si l’indicateur FLUSH_DOWNLOAD passe une visionneuse à distance, la méthode **FlushQueues** doit définir les bits STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="a6458-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="a6458-150">**FlushQueues** doit renvoyer puis S_OK.</span><span class="sxs-lookup"><span data-stu-id="a6458-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="a6458-151">Le spouleur MAPI lance les actions appropriées pour charger et télécharger des messages.</span><span class="sxs-lookup"><span data-stu-id="a6458-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6458-152">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="a6458-152">Notes to callers</span></span>

<span data-ttu-id="a6458-153">Un appel à l’objet de l’état du spouleur MAPI est une directive pour transférer tous les messages vers ou à partir du fournisseur de transport approprié.</span><span class="sxs-lookup"><span data-stu-id="a6458-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="a6458-154">Lorsque vous appelez objet d’état d’un fournisseur de transport individuels, seuls les messages de ce fournisseur sont affectés.</span><span class="sxs-lookup"><span data-stu-id="a6458-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6458-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6458-155">See also</span></span>



[<span data-ttu-id="a6458-156">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="a6458-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="a6458-157">Propriété canonique PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="a6458-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="a6458-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a6458-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

