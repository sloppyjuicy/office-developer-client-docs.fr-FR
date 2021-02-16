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
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414157"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="721b2-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="721b2-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="721b2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="721b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="721b2-105">Informe le fournisseur de transport que lepooler MAPI a terminé son traitement sur un message sortant.</span><span class="sxs-lookup"><span data-stu-id="721b2-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="721b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="721b2-106">Parameters</span></span>

 <span data-ttu-id="721b2-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="721b2-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="721b2-108">[in] Valeur de référence spécifique au message obtenue lors d’un appel précédent à la méthode [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="721b2-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="721b2-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="721b2-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="721b2-110">[out] Masque de bits d’indicateurs qui indique aupooler MAPI ce qu’il doit faire avec le message.</span><span class="sxs-lookup"><span data-stu-id="721b2-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="721b2-111">Si aucun indicateur n’est définie, le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="721b2-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="721b2-112">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="721b2-112">The following flags can be set:</span></span>
    
<span data-ttu-id="721b2-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="721b2-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="721b2-114">Pour l’instant, le fournisseur de transport dispose de toutes les informations nécessaires sur ce message.</span><span class="sxs-lookup"><span data-stu-id="721b2-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="721b2-115">Lorsque le fournisseur de transport requiert plus d’informations ou lorsqu’il a envoyé le message, il avertit lepooler MAPI en appelant la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’indicateur NOTIFY_SENTDEFERRED et en passant l’identificateur d’entrée du message.</span><span class="sxs-lookup"><span data-stu-id="721b2-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="721b2-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="721b2-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="721b2-117">Le fournisseur de transport n’envoie pas le message pour le moment pour des raisons qui ne sont pas des conditions d’erreur.</span><span class="sxs-lookup"><span data-stu-id="721b2-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="721b2-118">Le fournisseur de transport doit être appelé à nouveau ultérieurement pour envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="721b2-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="721b2-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="721b2-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="721b2-120">Le fournisseur de transport doit redémarrer le message qui lui a été transmis dans un appel de méthode [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="721b2-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="721b2-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="721b2-121">Return value</span></span>

<span data-ttu-id="721b2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="721b2-122">S_OK</span></span> 
  
> <span data-ttu-id="721b2-123">L’appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="721b2-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="721b2-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="721b2-124">Remarks</span></span>

<span data-ttu-id="721b2-125">Lepooler MAPI appelle la méthode **IXPLogon::EndMessage** après avoir terminé le traitement impliqué dans la fourniture d’informations de remise étendues ou de non remise.</span><span class="sxs-lookup"><span data-stu-id="721b2-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="721b2-126">Une fois que cet appel est revenu, la valeur dans le  _paramètre ulMsgRef_ n’est plus valide pour ce message.</span><span class="sxs-lookup"><span data-stu-id="721b2-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="721b2-127">Le fournisseur de transport peut réutiliser la même valeur sur un message futur.</span><span class="sxs-lookup"><span data-stu-id="721b2-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="721b2-128">Tous les objets que le fournisseur de transport ouvre lors du transfert d’un message doivent être libérés avant le retour de l’appel **EndMessage,** à l’exception de l’objet message que lepooler MAPI transmet au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="721b2-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="721b2-129">L’objet message transmis par lepooler MAPI n’est pas valide après **l’appel EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="721b2-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="721b2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="721b2-130">See also</span></span>



[<span data-ttu-id="721b2-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="721b2-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="721b2-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="721b2-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="721b2-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="721b2-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="721b2-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="721b2-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

