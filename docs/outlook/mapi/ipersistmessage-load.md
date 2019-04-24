---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317128"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="8d527-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="8d527-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="8d527-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d527-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d527-105">Charge le formulaire pour un message spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d527-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8d527-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d527-106">Parameters</span></span>

 <span data-ttu-id="8d527-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="8d527-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="8d527-108">dans Pointeur vers le site de messagerie du formulaire à charger.</span><span class="sxs-lookup"><span data-stu-id="8d527-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="8d527-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="8d527-109">_pMessage_</span></span>
  
> <span data-ttu-id="8d527-110">dans Pointeur vers le message pour lequel le formulaire doit être chargé.</span><span class="sxs-lookup"><span data-stu-id="8d527-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="8d527-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="8d527-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="8d527-112">dans Masque de bits des indicateurs définis par le client ou par le fournisseur, copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message, qui fournit des informations sur l'état du message.</span><span class="sxs-lookup"><span data-stu-id="8d527-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="8d527-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="8d527-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="8d527-114">dans Masque de binaire des indicateurs, copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message, qui fournit des informations supplémentaires sur l'état du message.</span><span class="sxs-lookup"><span data-stu-id="8d527-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d527-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d527-115">Return value</span></span>

<span data-ttu-id="8d527-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d527-116">S_OK</span></span> 
  
> <span data-ttu-id="8d527-117">Le formulaire a été chargé.</span><span class="sxs-lookup"><span data-stu-id="8d527-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d527-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d527-118">Remarks</span></span>

<span data-ttu-id="8d527-119">Les visionneuses de formulaires appellent la méthode **IPersistMessage:: Load** pour charger un formulaire pour un message existant.</span><span class="sxs-lookup"><span data-stu-id="8d527-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8d527-120">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8d527-120">Notes to implementers</span></span>

 <span data-ttu-id="8d527-121">Le **chargement** est appelé uniquement lorsqu'un formulaire se trouve dans l'un des États suivants:</span><span class="sxs-lookup"><span data-stu-id="8d527-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="8d527-122">Non initialisée</span><span class="sxs-lookup"><span data-stu-id="8d527-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="8d527-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8d527-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="8d527-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="8d527-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="8d527-125">Si une visionneuse de formulaires appelle **Load** alors que le formulaire est dans un autre État, la méthode renvoie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8d527-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="8d527-126">Si votre formulaire comporte une référence à un site de messagerie actif autre que celui qui est transmis en **chargement**, libérez le site d'origine car il ne sera plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="8d527-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="8d527-127">Stockez les pointeurs sur le site de messagerie et le message des paramètres _pMessageSite_ et _pMessage_ et appelez les deux méthodes « [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) » pour incrémenter leur nombre de références.</span><span class="sxs-lookup"><span data-stu-id="8d527-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="8d527-128">Une fois que **AddRef** est terminé, stockez les propriétés des paramètres _ulMessageStatus_ et _ulMessageFlags_ dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8d527-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="8d527-129">Faire basculer le formulaire à son état [normal](normal-state.md) avant de l'afficher et notifier les visionneuses inscrites en appelant leurs méthodes [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="8d527-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="8d527-130">Si aucune erreur ne se produit, retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="8d527-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d527-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d527-131">See also</span></span>



[<span data-ttu-id="8d527-132">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="8d527-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="8d527-133">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="8d527-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="8d527-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d527-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="8d527-135">État non initialisé</span><span class="sxs-lookup"><span data-stu-id="8d527-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="8d527-136">État HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8d527-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="8d527-137">État HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="8d527-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="8d527-138">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="8d527-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="8d527-139">IPersistStorage:: Load</span><span class="sxs-lookup"><span data-stu-id="8d527-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="8d527-140">IPersistStream:: Load</span><span class="sxs-lookup"><span data-stu-id="8d527-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="8d527-141">IPersistFile:: Load</span><span class="sxs-lookup"><span data-stu-id="8d527-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

