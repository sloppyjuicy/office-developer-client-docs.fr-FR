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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317128"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="3ede3-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="3ede3-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="3ede3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ede3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ede3-105">Charge le formulaire pour un message spécifié.</span><span class="sxs-lookup"><span data-stu-id="3ede3-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3ede3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3ede3-106">Parameters</span></span>

 <span data-ttu-id="3ede3-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="3ede3-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="3ede3-108">[in] Pointeur vers le site de message pour le formulaire à charger.</span><span class="sxs-lookup"><span data-stu-id="3ede3-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="3ede3-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="3ede3-109">_pMessage_</span></span>
  
> <span data-ttu-id="3ede3-110">[in] Pointeur vers le message pour lequel le formulaire doit être chargé.</span><span class="sxs-lookup"><span data-stu-id="3ede3-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="3ede3-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="3ede3-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="3ede3-112">[in] Masque de bits d’indicateurs définis par le client ou par un fournisseur, copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)du message, qui fournissent des informations sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="3ede3-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="3ede3-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="3ede3-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="3ede3-114">[in] Masque de bits d’indicateurs, copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)du message, qui fournit des informations supplémentaires sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="3ede3-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ede3-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3ede3-115">Return value</span></span>

<span data-ttu-id="3ede3-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ede3-116">S_OK</span></span> 
  
> <span data-ttu-id="3ede3-117">Le formulaire a été chargé avec succès.</span><span class="sxs-lookup"><span data-stu-id="3ede3-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ede3-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="3ede3-118">Remarks</span></span>

<span data-ttu-id="3ede3-119">Les visionneuses de formulaires appellent la méthode **IPersistMessage::Load** pour charger un formulaire pour un message existant.</span><span class="sxs-lookup"><span data-stu-id="3ede3-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ede3-120">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3ede3-120">Notes to implementers</span></span>

 <span data-ttu-id="3ede3-121">**Le** chargement est appelé uniquement lorsqu’un formulaire se trouve dans l’un des états suivants :</span><span class="sxs-lookup"><span data-stu-id="3ede3-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="3ede3-122">Nonnitialisé</span><span class="sxs-lookup"><span data-stu-id="3ede3-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="3ede3-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="3ede3-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="3ede3-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3ede3-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="3ede3-125">Si une visionneuse de formulaire appelle **Load** alors que le formulaire est dans un autre état, la méthode renvoie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="3ede3-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="3ede3-126">Si votre formulaire a une référence à un site de message actif autre que celui qui est transmis au chargement **,** libèrez le site d’origine car il ne sera plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ede3-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="3ede3-127">Stockez les pointeurs vers le site de message et le message à partir des paramètres  _pMessageSite_ et  _pMessage_ et appelez les méthodes [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) des deux objets pour incrémenter leur nombre de références.</span><span class="sxs-lookup"><span data-stu-id="3ede3-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="3ede3-128">Une **fois AddRef** terminé, stockez les propriétés des  _paramètres ulMessageStatus_ et  _ulMessageFlags_ dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3ede3-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="3ede3-129">Transition du formulaire vers son état [Normal](normal-state.md) avant de l’afficher et avertir les visionneuses inscrites en appelant leurs méthodes [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md)</span><span class="sxs-lookup"><span data-stu-id="3ede3-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="3ede3-130">Si aucune erreur ne se produit, renvoyez S_OK.</span><span class="sxs-lookup"><span data-stu-id="3ede3-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ede3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ede3-131">See also</span></span>



[<span data-ttu-id="3ede3-132">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="3ede3-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="3ede3-133">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3ede3-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="3ede3-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ede3-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="3ede3-135">État nonnitialisé</span><span class="sxs-lookup"><span data-stu-id="3ede3-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="3ede3-136">HandsOffAfterSave, état</span><span class="sxs-lookup"><span data-stu-id="3ede3-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="3ede3-137">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="3ede3-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="3ede3-138">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="3ede3-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="3ede3-139">IPersistStorage::Load</span><span class="sxs-lookup"><span data-stu-id="3ede3-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="3ede3-140">IPersistStream::Load</span><span class="sxs-lookup"><span data-stu-id="3ede3-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="3ede3-141">IPersistFile::Load</span><span class="sxs-lookup"><span data-stu-id="3ede3-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

