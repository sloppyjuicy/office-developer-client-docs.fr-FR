---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 40a72bed0b3e763ea482b228174b85d9f42185c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784105"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="917de-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="917de-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="917de-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="917de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="917de-105">Indique que le message en cours a été soumis au spouleur MAPI à la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="917de-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="917de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="917de-106">Parameters</span></span>

<span data-ttu-id="917de-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="917de-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="917de-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="917de-108">Return value</span></span>

<span data-ttu-id="917de-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="917de-109">S_OK</span></span> 
  
> <span data-ttu-id="917de-110">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="917de-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="917de-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="917de-111">Remarks</span></span>

<span data-ttu-id="917de-112">Un objet form appelle la méthode **IMAPIViewAdviseSink::OnSubmitted** après qu’un appel à [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) a réussi.</span><span class="sxs-lookup"><span data-stu-id="917de-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="917de-113">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="917de-113">Notes to implementers</span></span>

<span data-ttu-id="917de-114">Après avoir appelé **OnSubmitted** , vous pouvez continuer sur l’hypothèse que le message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="917de-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="917de-115">Mettre à jour votre windows afin de refléter les modifications qui se sont produites.</span><span class="sxs-lookup"><span data-stu-id="917de-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="917de-116">Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="917de-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="917de-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="917de-117">See also</span></span>



[<span data-ttu-id="917de-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="917de-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="917de-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="917de-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

