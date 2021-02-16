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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433982"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="7a5b2-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="7a5b2-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="7a5b2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a5b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a5b2-105">Avertit la visionneuse de formulaire que le message actuel a été envoyé aupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="7a5b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a5b2-106">Parameters</span></span>

<span data-ttu-id="7a5b2-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="7a5b2-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="7a5b2-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7a5b2-108">Return value</span></span>

<span data-ttu-id="7a5b2-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a5b2-109">S_OK</span></span> 
  
> <span data-ttu-id="7a5b2-110">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a5b2-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="7a5b2-111">Remarks</span></span>

<span data-ttu-id="7a5b2-112">Un objet de formulaire appelle la méthode **IMAPIViewAdviseSink::OnSubmitted** après qu’un appel à [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a5b2-113">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="7a5b2-113">Notes to implementers</span></span>

<span data-ttu-id="7a5b2-114">Après **avoir appelé OnSubmitted,** vous pouvez continuer sur l’hypothèse que le message a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="7a5b2-115">Mettez à jour vos fenêtres pour refléter les modifications qui se sont produites.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="7a5b2-116">Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7a5b2-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a5b2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a5b2-117">See also</span></span>



[<span data-ttu-id="7a5b2-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="7a5b2-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="7a5b2-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a5b2-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

