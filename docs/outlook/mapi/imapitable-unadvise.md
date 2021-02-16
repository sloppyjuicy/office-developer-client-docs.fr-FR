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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430230"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="5bd68-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5bd68-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="5bd68-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bd68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bd68-105">Annule l’envoi de notifications précédemment définies avec un appel à la [méthode IMAPITable::Advise.](imapitable-advise.md)</span><span class="sxs-lookup"><span data-stu-id="5bd68-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5bd68-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bd68-106">Parameters</span></span>

 <span data-ttu-id="5bd68-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="5bd68-107">_ulConnection_</span></span>
  
> <span data-ttu-id="5bd68-108">[in] Numéro de la connexion d’inscription renvoyée par un appel [à IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="5bd68-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5bd68-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5bd68-109">Return value</span></span>

<span data-ttu-id="5bd68-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bd68-110">S_OK</span></span> 
  
> <span data-ttu-id="5bd68-111">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="5bd68-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bd68-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="5bd68-112">Remarks</span></span>

<span data-ttu-id="5bd68-113">Utilisez la méthode **IMAPITable::Unadvise** pour libérer le pointeur vers l’objet de réception de notification transmis dans le paramètre  _lpAdviseSink_ dans l’appel précédent à **IMAPITable::Advise,** ce qui annule l’inscription d’une notification.</span><span class="sxs-lookup"><span data-stu-id="5bd68-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="5bd68-114">Dans le cadre de l’ignorer, la méthode **IUnknown::Release** de l’objet est appelée.</span><span class="sxs-lookup"><span data-stu-id="5bd68-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="5bd68-115">En règle générale, **Release** est appelé pendant l’appel **Unadvise,** mais si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour le sink de conseil, l’appel **de** publication est retardé jusqu’à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="5bd68-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="5bd68-116">Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="5bd68-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="5bd68-117">Pour plus d’informations sur les notifications de tableau, voir [À propos des notifications de tableau.](about-table-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="5bd68-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="5bd68-118">Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Notification d’événement de prise en charge.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="5bd68-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5bd68-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5bd68-119">MFCMAPI reference</span></span>

<span data-ttu-id="5bd68-120">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5bd68-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5bd68-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5bd68-121">**File**</span></span>|<span data-ttu-id="5bd68-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5bd68-122">**Function**</span></span>|<span data-ttu-id="5bd68-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5bd68-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5bd68-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="5bd68-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5bd68-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="5bd68-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="5bd68-126">MFCMAPI utilise la **méthode IMAPITable::Unadvise** pour annuler les notifications pour la table.</span><span class="sxs-lookup"><span data-stu-id="5bd68-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bd68-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bd68-127">See also</span></span>



[<span data-ttu-id="5bd68-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5bd68-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5bd68-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="5bd68-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="5bd68-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bd68-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="5bd68-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5bd68-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

