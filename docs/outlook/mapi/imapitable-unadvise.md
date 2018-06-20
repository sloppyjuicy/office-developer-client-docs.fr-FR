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
ms.openlocfilehash: e9d8565cfaa17764e92bddafb29e744d23872515
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784114"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="116e4-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="116e4-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="116e4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="116e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="116e4-105">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMAPITable::Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="116e4-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="116e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="116e4-106">Parameters</span></span>

 <span data-ttu-id="116e4-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="116e4-107">_ulConnection_</span></span>
  
> <span data-ttu-id="116e4-108">[in] Le numéro de la connexion d’enregistrement renvoyé par un appel à [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="116e4-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="116e4-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="116e4-109">Return value</span></span>

<span data-ttu-id="116e4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="116e4-110">S_OK</span></span> 
  
> <span data-ttu-id="116e4-111">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="116e4-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="116e4-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="116e4-112">Remarks</span></span>

<span data-ttu-id="116e4-113">Utilisez la méthode **IMAPITable::Unadvise** pour libérer le pointeur vers l’objet de récepteur advise transmis dans le paramètre _lpAdviseSink_ dans l’appel précédent à **IMAPITable::Advise**, annulant ainsi un enregistrement de notification.</span><span class="sxs-lookup"><span data-stu-id="116e4-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="116e4-114">Dans le cadre d’ignorer le pointeur vers l’objet de récepteur advise, la méthode l’objet **IUnknown::Release** est appelée.</span><span class="sxs-lookup"><span data-stu-id="116e4-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="116e4-115">En règle générale, la **version** est appelé pendant l’appel **Unadvise** , mais si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour le récepteur de notifications, l’appel de la **version** est différée jusqu'à **OnNotify** méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="116e4-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="116e4-116">Pour plus d’informations sur le processus de notification, voir [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="116e4-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="116e4-117">Pour obtenir des informations spécifiques sur la notification de la table, voir [Sur les Notifications de Table](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="116e4-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="116e4-118">Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Prise en charge de Notification d’événement](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="116e4-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="116e4-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="116e4-119">MFCMAPI reference</span></span>

<span data-ttu-id="116e4-120">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="116e4-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="116e4-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="116e4-121">**File**</span></span>|<span data-ttu-id="116e4-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="116e4-122">**Function**</span></span>|<span data-ttu-id="116e4-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="116e4-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="116e4-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="116e4-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="116e4-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="116e4-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="116e4-126">MFCMAPI utilise la méthode **IMAPITable::Unadvise** pour annuler des notifications pour la table.</span><span class="sxs-lookup"><span data-stu-id="116e4-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="116e4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="116e4-127">See also</span></span>



[<span data-ttu-id="116e4-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="116e4-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="116e4-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="116e4-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="116e4-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="116e4-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="116e4-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="116e4-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

