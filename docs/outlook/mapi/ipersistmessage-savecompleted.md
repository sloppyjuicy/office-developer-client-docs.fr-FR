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
ms.openlocfilehash: 7a82ce9a46017993adfc6c4c755b6c97b847e579
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784371"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="15dc1-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="15dc1-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="15dc1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15dc1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15dc1-105">Avertit le formulaire qui un enregistrement opération a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="15dc1-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="15dc1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15dc1-106">Parameters</span></span>

<span data-ttu-id="15dc1-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="15dc1-107">_pMessage_</span></span>
  
> <span data-ttu-id="15dc1-108">[in] Pointeur vers le message nouvellement enregistré.</span><span class="sxs-lookup"><span data-stu-id="15dc1-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15dc1-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="15dc1-109">Return value</span></span>

<span data-ttu-id="15dc1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="15dc1-110">S_OK</span></span> 
  
> <span data-ttu-id="15dc1-111">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="15dc1-111">The notification was successful.</span></span>
    
<span data-ttu-id="15dc1-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="15dc1-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="15dc1-113">Le paramètre _pMessage_ est NULL, le formulaire est soit à l’état [HandsOffFromNormal](handsofffromnormal-state.md) ou [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="15dc1-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="15dc1-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="15dc1-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="15dc1-115">Le formulaire n’est pas dans un des états suivants :</span><span class="sxs-lookup"><span data-stu-id="15dc1-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="15dc1-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="15dc1-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="15dc1-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="15dc1-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="15dc1-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="15dc1-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="15dc1-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="15dc1-119">Remarks</span></span>

<span data-ttu-id="15dc1-120">La méthode **IPersistMessage::SaveCompleted** est appelée par une visionneuse de formulaire pour notifier le formulaire toutes les modifications en attente ont été enregistrées.</span><span class="sxs-lookup"><span data-stu-id="15dc1-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="15dc1-121">**Méthode SaveCompleted** doit être appelée uniquement lorsque le formulaire est dans un des états suivants :</span><span class="sxs-lookup"><span data-stu-id="15dc1-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="15dc1-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="15dc1-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="15dc1-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="15dc1-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="15dc1-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="15dc1-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="15dc1-125">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="15dc1-125">Notes to implementers</span></span>

<span data-ttu-id="15dc1-126">Il existe plusieurs actions possibles que la méthode de la **méthode SaveCompleted** peut effectuer, selon le message le paramètre de pointeur contient et état le message se trouve dans.</span><span class="sxs-lookup"><span data-stu-id="15dc1-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="15dc1-127">Toutefois, lorsqu’une action réussit, toujours enregistrer l’état actuel du message vers laquelle pointe le paramètre _pMessage_ et transition du formulaire à son état [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="15dc1-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="15dc1-128">Le tableau suivant décrit les conditions qui affectent les actions à qu'entreprendre dans votre implémentation de la **méthode SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="15dc1-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="15dc1-129">**Condition**</span><span class="sxs-lookup"><span data-stu-id="15dc1-129">**Condition**</span></span>|<span data-ttu-id="15dc1-130">**Action**</span><span class="sxs-lookup"><span data-stu-id="15dc1-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15dc1-131">Le paramètre _pMessage_ est NULL, et le paramètre _fSameAsLoad_ de la méthode [IPersistMessage::Save](ipersistmessage-save.md) est défini sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="15dc1-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="15dc1-132">Appelez la méthode [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de tous les utilisateurs inscrits, marquer le formulaire en tant que S_OK clean et de retour.</span><span class="sxs-lookup"><span data-stu-id="15dc1-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="15dc1-133">Le paramètre _pMessage_ est NULL, et le paramètre _fSameAsLoad_ de la méthode **IPersistMessage::Save** est défini sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="15dc1-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="15dc1-134">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="15dc1-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="15dc1-135">Le formulaire est dans l’état HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="15dc1-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="15dc1-136">Libérer le message en cours et remplacez-le par le message vers laquelle pointé le paramètre _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="15dc1-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="15dc1-137">Appelez la méthode [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) du message de remplacement et qu’elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="15dc1-137">Call the replacement message's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="15dc1-138">Le formulaire est dans l’état HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="15dc1-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="15dc1-139">Appelez la méthode **IMAPIViewAdviseSink::OnSaved** de tous les utilisateurs inscrits, marquer le formulaire en tant que S_OK clean et de retour.</span><span class="sxs-lookup"><span data-stu-id="15dc1-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="15dc1-140">Le formulaire est dans l’état [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="15dc1-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="15dc1-141">Libérer le message en cours et remplacez-le par le message vers lequel pointé _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="15dc1-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="15dc1-142">Appeler la méthode **IUnknown::AddRef** du message de remplacement.</span><span class="sxs-lookup"><span data-stu-id="15dc1-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="15dc1-143">Appelez la méthode **IMAPIViewAdviseSink::OnSaved** de tous les utilisateurs inscrits, marquer le formulaire en tant que S_OK clean et de retour.</span><span class="sxs-lookup"><span data-stu-id="15dc1-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="15dc1-144">Le formulaire est dans un des États HandsOff et le paramètre _pMessage_ est défini sur NULL.</span><span class="sxs-lookup"><span data-stu-id="15dc1-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="15dc1-145">Retour E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="15dc1-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="15dc1-146">Le formulaire est dans un état autre qu’un des États HandsOff ou l’état NoScribble.</span><span class="sxs-lookup"><span data-stu-id="15dc1-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="15dc1-147">Retourner E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="15dc1-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="15dc1-148">Pour plus d’informations sur l’enregistrement des objets de stockage, voir la documentation pour les méthodes [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) ou [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="15dc1-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) or [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15dc1-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15dc1-149">See also</span></span>



[<span data-ttu-id="15dc1-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15dc1-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="15dc1-151">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="15dc1-151">Form States</span></span>](form-states.md)


[<span data-ttu-id="15dc1-152">IPersistStorage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="15dc1-152">IPersistStorage::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)
  
[<span data-ttu-id="15dc1-153">IPersistFile::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="15dc1-153">IPersistFile::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)

