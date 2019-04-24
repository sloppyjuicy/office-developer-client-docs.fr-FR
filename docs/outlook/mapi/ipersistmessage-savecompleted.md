---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317135"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="3dd38-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="3dd38-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="3dd38-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dd38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dd38-105">Avertit le formulaire qu'une opération d'enregistrement a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="3dd38-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="3dd38-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dd38-106">Parameters</span></span>

<span data-ttu-id="3dd38-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="3dd38-107">_pMessage_</span></span>
  
> <span data-ttu-id="3dd38-108">dans Pointeur vers le message nouvellement enregistré.</span><span class="sxs-lookup"><span data-stu-id="3dd38-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3dd38-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3dd38-109">Return value</span></span>

<span data-ttu-id="3dd38-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3dd38-110">S_OK</span></span> 
  
> <span data-ttu-id="3dd38-111">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="3dd38-111">The notification was successful.</span></span>
    
<span data-ttu-id="3dd38-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3dd38-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="3dd38-113">Le paramètre _pMessage_ est null et le formulaire est dans l'état [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="3dd38-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="3dd38-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="3dd38-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="3dd38-115">Le formulaire n'est pas dans l'un des États suivants:</span><span class="sxs-lookup"><span data-stu-id="3dd38-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="3dd38-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3dd38-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="3dd38-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="3dd38-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="3dd38-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="3dd38-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="3dd38-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="3dd38-119">Remarks</span></span>

<span data-ttu-id="3dd38-120">La méthode **IPersistMessage:: SaveCompleted** est appelée par une visionneuse de formulaires pour informer le formulaire que toutes les modifications en attente ont été enregistrées.</span><span class="sxs-lookup"><span data-stu-id="3dd38-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="3dd38-121">**SaveCompleted** doit être appelé uniquement lorsque le formulaire est dans l'un des États suivants:</span><span class="sxs-lookup"><span data-stu-id="3dd38-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="3dd38-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3dd38-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="3dd38-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="3dd38-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="3dd38-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="3dd38-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="3dd38-125">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3dd38-125">Notes to implementers</span></span>

<span data-ttu-id="3dd38-126">La méthode **SaveCompleted** peut effectuer plusieurs actions en fonction de ce que contient le paramètre pointeur de message et de l'État dans lequel se trouve le message.</span><span class="sxs-lookup"><span data-stu-id="3dd38-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="3dd38-127">Toutefois, lorsqu'une action réussit, toujours enregistrer l'état actuel du message vers lequel pointe le paramètre _pMessage_ et le faire passer à son état [normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="3dd38-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="3dd38-128">Le tableau suivant décrit les conditions qui affectent les actions que vous devez suivre lors de l'implémentation de **SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="3dd38-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="3dd38-129">**Condition**</span><span class="sxs-lookup"><span data-stu-id="3dd38-129">**Condition**</span></span>|<span data-ttu-id="3dd38-130">**Action**</span><span class="sxs-lookup"><span data-stu-id="3dd38-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3dd38-131">Le paramètre _pMessage_ est null et le paramètre _fSameAsLoad_ de la méthode [IPersistMessage:: Save](ipersistmessage-save.md) est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="3dd38-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="3dd38-132">Appelez la méthode [IMAPIViewAdviseSink:: OnSaved](imapiviewadvisesink-onsaved.md) de toutes les visionneuses inscrites, marquez le formulaire comme Clean et renvoyez S_OK.</span><span class="sxs-lookup"><span data-stu-id="3dd38-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3dd38-133">Le paramètre _pMessage_ est null et le paramètre _fSameAsLoad_ de la méthode **IPersistMessage:: Save** est défini sur false.</span><span class="sxs-lookup"><span data-stu-id="3dd38-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="3dd38-134">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="3dd38-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3dd38-135">Le formulaire est dans l'État HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="3dd38-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="3dd38-136">ReLâchez le message en cours et remplacez-le par le message désigné par le paramètre _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="3dd38-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="3dd38-137">Appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) du message et retournez S_OK.</span><span class="sxs-lookup"><span data-stu-id="3dd38-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3dd38-138">Le formulaire est dans l'État HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="3dd38-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="3dd38-139">Appelez la méthode **IMAPIViewAdviseSink:: OnSaved** de toutes les visionneuses inscrites, marquez le formulaire comme Clean et renvoyez S_OK.</span><span class="sxs-lookup"><span data-stu-id="3dd38-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3dd38-140">Le formulaire est dans l' [](noscribble-state.md) État noscribble.</span><span class="sxs-lookup"><span data-stu-id="3dd38-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="3dd38-141">ReLâchez le message actif et remplacez-le par le message désigné par _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="3dd38-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="3dd38-142">Appelez la méthode **IUnknown:: AddRef** du message.</span><span class="sxs-lookup"><span data-stu-id="3dd38-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="3dd38-143">Appelez la méthode **IMAPIViewAdviseSink:: OnSaved** de toutes les visionneuses inscrites, marquez le formulaire comme Clean et renvoyez S_OK.</span><span class="sxs-lookup"><span data-stu-id="3dd38-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="3dd38-144">Le formulaire se trouve dans l'un des États HandsOff et le paramètre _pMessage_ est défini sur null.</span><span class="sxs-lookup"><span data-stu-id="3dd38-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="3dd38-145">Renvoie E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="3dd38-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="3dd38-146">Le formulaire est dans un État autre que l'un des États HandsOff ou l'État noScribble.</span><span class="sxs-lookup"><span data-stu-id="3dd38-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="3dd38-147">Renvoie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="3dd38-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="3dd38-148">Pour plus d'informations sur l'enregistrement d'objets de stockage, voir la documentation pour les méthodes [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) ou [IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) .</span><span class="sxs-lookup"><span data-stu-id="3dd38-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3dd38-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dd38-149">See also</span></span>

- [<span data-ttu-id="3dd38-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3dd38-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="3dd38-151">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="3dd38-151">Form States</span></span>](form-states.md)
