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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783744"
---
# <a name="imapiformadvise"></a><span data-ttu-id="ef765-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="ef765-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="ef765-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef765-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef765-105">Enregistre une visionneuse de formulaire pour les notifications concernant les événements qui affectent le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ef765-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ef765-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef765-106">Parameters</span></span>

 <span data-ttu-id="ef765-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="ef765-107">_pAdvise_</span></span>
  
> <span data-ttu-id="ef765-108">[in] Un pointeur vers un affichage de notification objet sink de recevoir des notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ef765-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="ef765-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="ef765-109">_pulConnection_</span></span>
  
> <span data-ttu-id="ef765-110">[out] Pointeur vers une valeur différente de zéro qui représente un enregistrement de notification réussie.</span><span class="sxs-lookup"><span data-stu-id="ef765-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef765-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ef765-111">Return value</span></span>

<span data-ttu-id="ef765-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef765-112">S_OK</span></span> 
  
> <span data-ttu-id="ef765-113">L’inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="ef765-113">The registration was successful.</span></span>
    
<span data-ttu-id="ef765-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="ef765-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="ef765-115">L’enregistrement a échoué en raison de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ef765-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef765-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ef765-116">Remarks</span></span>

<span data-ttu-id="ef765-117">Visionneuses de formulaire appellent méthode de **IMAPIForm::Advise** d’un formulaire à l’enregistrement d’une notification lorsque des modifications se produisent au formulaire.</span><span class="sxs-lookup"><span data-stu-id="ef765-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ef765-118">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ef765-118">Notes to implementers</span></span>

<span data-ttu-id="ef765-119">Conserver une copie de l’affichage de notification pointeur du récepteur transmis dans le paramètre _pAdvise_ afin que vous pouvez l’utiliser pour appeler la méthode [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) appropriée lorsqu’un événement se produit.</span><span class="sxs-lookup"><span data-stu-id="ef765-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="ef765-120">Appel de l’affichage de notification méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) du récepteur conserver le pointeur jusqu'à l’annulation de l’inscription aux notifications.</span><span class="sxs-lookup"><span data-stu-id="ef765-120">Call the view advise sink's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="ef765-121">Définir le contenu du paramètre _pulConnection_ à un nombre différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="ef765-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="ef765-122">De nombreux formulaires implémentent un objet d’assistance pour gérer l’enregistrement et la notification ultérieure d’événements.</span><span class="sxs-lookup"><span data-stu-id="ef765-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="ef765-123">Pour plus d’informations sur le processus de notification en général, voir [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ef765-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="ef765-124">Pour plus d’informations sur les formulaires et de notification, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ef765-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef765-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef765-125">See also</span></span>



[<span data-ttu-id="ef765-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ef765-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="ef765-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef765-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="ef765-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef765-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="ef765-129">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="ef765-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="ef765-130">Envoyer et recevoir des Notifications de formulaire</span><span class="sxs-lookup"><span data-stu-id="ef765-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

