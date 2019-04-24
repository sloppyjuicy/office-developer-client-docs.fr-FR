---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328804"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="ccb71-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ccb71-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="ccb71-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccb71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccb71-105">Annule l'envoi des notifications précédemment configurées avec un appel à la méthode [IMAPITable:: Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="ccb71-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ccb71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccb71-106">Parameters</span></span>

 <span data-ttu-id="ccb71-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="ccb71-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ccb71-108">dans Numéro de la connexion d'inscription renvoyée par un appel de la procédure [IMAPITable:: Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="ccb71-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ccb71-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ccb71-109">Return value</span></span>

<span data-ttu-id="ccb71-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccb71-110">S_OK</span></span> 
  
> <span data-ttu-id="ccb71-111">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="ccb71-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccb71-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="ccb71-112">Remarks</span></span>

<span data-ttu-id="ccb71-113">Utilisez la méthode **IMAPITable::** Unadvise pour libérer le pointeur vers l'objet de récepteur de notifications transmis dans le paramètre _lpAdviseSink_ de l'appel précédent à **IMAPITable:: Advise**, ce qui a pour effet d'annuler une inscription aux notifications.</span><span class="sxs-lookup"><span data-stu-id="ccb71-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="ccb71-114">Dans le cadre du rejet du pointeur vers l'objet de récepteur de notification, la méthode **IUnknown:: Release** de l'objet est appelée.</span><span class="sxs-lookup"><span data-stu-id="ccb71-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="ccb71-115">En règle générale, la **publication** est appelée pendant l'appel Unadvise, mais si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour le récepteur de notifications, l'appel de **libération** est retardé jusqu'à ce que l' **OnNotify** \*\*\*\* méthode renvoie.</span><span class="sxs-lookup"><span data-stu-id="ccb71-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="ccb71-116">Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ccb71-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="ccb71-117">Pour obtenir des informations spécifiques sur la notification de table, consultez la rubrique [à propos des notifications de table](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ccb71-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="ccb71-118">Pour plus d'informations sur l'utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez la rubrique [prise en](supporting-event-notification.md)charge des notifications d'événements.</span><span class="sxs-lookup"><span data-stu-id="ccb71-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ccb71-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ccb71-119">MFCMAPI reference</span></span>

<span data-ttu-id="ccb71-120">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ccb71-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ccb71-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ccb71-121">**File**</span></span>|<span data-ttu-id="ccb71-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ccb71-122">**Function**</span></span>|<span data-ttu-id="ccb71-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ccb71-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccb71-124">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="ccb71-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ccb71-125">CContentsTableListCtrl:: NotificationOff</span><span class="sxs-lookup"><span data-stu-id="ccb71-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="ccb71-126">MFCMAPI utilise la méthode **IMAPITable::** Unadvise pour annuler les notifications pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="ccb71-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccb71-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccb71-127">See also</span></span>



[<span data-ttu-id="ccb71-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ccb71-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ccb71-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="ccb71-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="ccb71-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccb71-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ccb71-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ccb71-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

