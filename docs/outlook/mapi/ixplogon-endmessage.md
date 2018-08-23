---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582468"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="591d5-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="591d5-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="591d5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="591d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="591d5-105">Informe le fournisseur de transport que le spouleur MAPI terminé son traitement d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="591d5-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="591d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="591d5-106">Parameters</span></span>

 <span data-ttu-id="591d5-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="591d5-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="591d5-108">[in] Une valeur de référence de message spécifique qui a été obtenue dans un appel précédent à la méthode [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="591d5-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="591d5-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="591d5-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="591d5-110">[out] Masque de bits d’indicateurs qui indique au spouleur MAPI quoi faire avec le message.</span><span class="sxs-lookup"><span data-stu-id="591d5-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="591d5-111">Si aucun indicateur est défini, le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="591d5-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="591d5-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="591d5-112">The following flags can be set:</span></span>
    
<span data-ttu-id="591d5-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="591d5-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="591d5-114">Le fournisseur de transport a toutes les informations nécessaires sur ce message pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="591d5-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="591d5-115">Lorsque le fournisseur de transport nécessite plus d’informations ou lorsqu’il a envoyé le message, il notifie le spouleur MAPI en appelant la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’indicateur NOTIFY_SENTDEFERRED et en transmettant l’identificateur d’entrée du message.</span><span class="sxs-lookup"><span data-stu-id="591d5-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="591d5-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="591d5-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="591d5-117">Le fournisseur de transport n’envoie pas le message à l’heure actuelle pour des raisons qui ne sont pas des conditions d’erreur.</span><span class="sxs-lookup"><span data-stu-id="591d5-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="591d5-118">Le fournisseur de transport doit être appelé à nouveau ultérieurement pour envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="591d5-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="591d5-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="591d5-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="591d5-120">Le fournisseur de transport doit redémarrer le message passé dans un appel de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="591d5-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="591d5-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="591d5-121">Return value</span></span>

<span data-ttu-id="591d5-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="591d5-122">S_OK</span></span> 
  
> <span data-ttu-id="591d5-123">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="591d5-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="591d5-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="591d5-124">Remarks</span></span>

<span data-ttu-id="591d5-125">Le spouleur MAPI appelle la méthode **IXPLogon::EndMessage** une fois le traitement entrent en jeu dans remise étendue ou les informations de non-remise.</span><span class="sxs-lookup"><span data-stu-id="591d5-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="591d5-126">Une fois que cet appel retourne la valeur dans le paramètre _ulMsgRef_ n’est plus valide pour ce message.</span><span class="sxs-lookup"><span data-stu-id="591d5-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="591d5-127">Le fournisseur de transport peut réutiliser la même valeur d’un message de futur.</span><span class="sxs-lookup"><span data-stu-id="591d5-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="591d5-128">Tous les objets qui le fournisseur de transport s’ouvre lors du transfert d’un message doivent être libérés avant le retour **EndMessage** , à l’exception de l’objet de message le spouleur MAPI transmet au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="591d5-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="591d5-129">L’objet du message sont transmise par le spouleur MAPI n’est pas valide après l’appel de **EndMessage** .</span><span class="sxs-lookup"><span data-stu-id="591d5-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="591d5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="591d5-130">See also</span></span>



[<span data-ttu-id="591d5-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="591d5-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="591d5-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="591d5-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="591d5-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="591d5-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="591d5-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="591d5-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

