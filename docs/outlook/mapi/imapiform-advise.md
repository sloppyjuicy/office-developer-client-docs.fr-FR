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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387530"
---
# <a name="imapiformadvise"></a><span data-ttu-id="b8ec8-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="b8ec8-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="b8ec8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8ec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8ec8-105">Enregistre une visionneuse de formulaire pour les notifications concernant les événements qui affectent le formulaire.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b8ec8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8ec8-106">Parameters</span></span>

 <span data-ttu-id="b8ec8-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="b8ec8-107">_pAdvise_</span></span>
  
> <span data-ttu-id="b8ec8-108">[in] Un pointeur vers un affichage de notification objet sink de recevoir des notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="b8ec8-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="b8ec8-109">_pulConnection_</span></span>
  
> <span data-ttu-id="b8ec8-110">[out] Pointeur vers une valeur différente de zéro qui représente un enregistrement de notification réussie.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8ec8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8ec8-111">Return value</span></span>

<span data-ttu-id="b8ec8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8ec8-112">S_OK</span></span> 
  
> <span data-ttu-id="b8ec8-113">L’inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-113">The registration was successful.</span></span>
    
<span data-ttu-id="b8ec8-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b8ec8-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="b8ec8-115">L’enregistrement a échoué en raison de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8ec8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8ec8-116">Remarks</span></span>

<span data-ttu-id="b8ec8-117">Visionneuses de formulaire appellent méthode de **IMAPIForm::Advise** d’un formulaire à l’enregistrement d’une notification lorsque des modifications se produisent au formulaire.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b8ec8-118">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b8ec8-118">Notes to implementers</span></span>

<span data-ttu-id="b8ec8-119">Conserver une copie de l’affichage de notification pointeur du récepteur transmis dans le paramètre _pAdvise_ afin que vous pouvez l’utiliser pour appeler la méthode [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) appropriée lorsqu’un événement se produit.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="b8ec8-120">Appel de l’affichage de notification méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) du récepteur conserver le pointeur jusqu'à l’annulation de l’inscription aux notifications.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="b8ec8-121">Définir le contenu du paramètre _pulConnection_ à un nombre différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="b8ec8-122">De nombreux formulaires implémentent un objet d’assistance pour gérer l’enregistrement et la notification ultérieure d’événements.</span><span class="sxs-lookup"><span data-stu-id="b8ec8-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="b8ec8-123">Pour plus d’informations sur le processus de notification en général, voir [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b8ec8-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="b8ec8-124">Pour plus d’informations sur les formulaires et de notification, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b8ec8-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8ec8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8ec8-125">See also</span></span>



[<span data-ttu-id="b8ec8-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b8ec8-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="b8ec8-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8ec8-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="b8ec8-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8ec8-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="b8ec8-129">Notification d’événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="b8ec8-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="b8ec8-130">Envoi et réception de notifications de formulaire</span><span class="sxs-lookup"><span data-stu-id="b8ec8-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

