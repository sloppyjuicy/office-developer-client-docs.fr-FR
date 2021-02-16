---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329483"
---
# <a name="imapiformadvise"></a><span data-ttu-id="c0e36-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="c0e36-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="c0e36-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0e36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0e36-105">Inscrit une visionneuse de formulaires pour les notifications sur les événements qui affectent le formulaire.</span><span class="sxs-lookup"><span data-stu-id="c0e36-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c0e36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0e36-106">Parameters</span></span>

 <span data-ttu-id="c0e36-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="c0e36-107">_pAdvise_</span></span>
  
> <span data-ttu-id="c0e36-108">[in] Un pointeur vers une vue conseille à l’objet de réception de recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0e36-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="c0e36-109">_connection_</span><span class="sxs-lookup"><span data-stu-id="c0e36-109">_pulConnection_</span></span>
  
> <span data-ttu-id="c0e36-110">[out] Pointeur vers une valeur autre que zéro qui représente une inscription de notification réussie.</span><span class="sxs-lookup"><span data-stu-id="c0e36-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0e36-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c0e36-111">Return value</span></span>

<span data-ttu-id="c0e36-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0e36-112">S_OK</span></span> 
  
> <span data-ttu-id="c0e36-113">L’inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="c0e36-113">The registration was successful.</span></span>
    
<span data-ttu-id="c0e36-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c0e36-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="c0e36-115">L’inscription a échoué en raison d’une mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="c0e36-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0e36-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0e36-116">Remarks</span></span>

<span data-ttu-id="c0e36-117">Les visionneuses de formulaire appellent la méthode **IMAPIForm::Advise** d’un formulaire pour s’inscrire aux notifications lorsque des modifications sont apportées au formulaire.</span><span class="sxs-lookup"><span data-stu-id="c0e36-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c0e36-118">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c0e36-118">Notes to implementers</span></span>

<span data-ttu-id="c0e36-119">Conservez une copie du pointeur de l’affichage conseillé transmis dans le paramètre  _pAdvise_ afin de pouvoir l’utiliser pour appeler la méthode [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) appropriée lorsqu’un événement se produit.</span><span class="sxs-lookup"><span data-stu-id="c0e36-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="c0e36-120">Appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l’affichage pour conserver le pointeur jusqu’à l’annulation de l’inscription de la notification.</span><span class="sxs-lookup"><span data-stu-id="c0e36-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="c0e36-121">Définissez le contenu du  _paramètreconnection sur_ un nombre autre que zéro.</span><span class="sxs-lookup"><span data-stu-id="c0e36-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="c0e36-122">De nombreux formulaires implémentent un objet d’aide pour gérer l’inscription et la notification ultérieure des événements.</span><span class="sxs-lookup"><span data-stu-id="c0e36-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="c0e36-123">Pour plus d’informations sur le processus de notification en général, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c0e36-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="c0e36-124">Pour plus d’informations sur les notifications et les [formulaires,](sending-and-receiving-form-notifications.md)voir Sending and Receiving Form Notifications .</span><span class="sxs-lookup"><span data-stu-id="c0e36-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0e36-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0e36-125">See also</span></span>



[<span data-ttu-id="c0e36-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c0e36-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="c0e36-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0e36-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="c0e36-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0e36-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="c0e36-129">Notification d’événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="c0e36-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="c0e36-130">Envoi et réception de notifications de formulaire</span><span class="sxs-lookup"><span data-stu-id="c0e36-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

