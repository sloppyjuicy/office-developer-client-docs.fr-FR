---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bdda950cd1fab66db46590e0b9141bb3d2a75221
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784247"
---
# <a name="imsgstorenotifynewmail"></a><span data-ttu-id="fe586-103">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="fe586-103">IMsgStore::NotifyNewMail</span></span>

  
  
<span data-ttu-id="fe586-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe586-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe586-p101">Informe la banque de messages un nouveau message est arriv�. Cette m�thode est appel�e uniquement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe586-p101">Informs the message store that a new message has arrived. This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a><span data-ttu-id="fe586-107">Param�tres</span><span class="sxs-lookup"><span data-stu-id="fe586-107">Parameters</span></span>

 <span data-ttu-id="fe586-108">_lpNotification_</span><span class="sxs-lookup"><span data-stu-id="fe586-108">_lpNotification_</span></span>
  
> <span data-ttu-id="fe586-109">[in] Pointeur vers une structure [NOTIFICATION](notification.md) qui d�crit la notification de nouveau message.</span><span class="sxs-lookup"><span data-stu-id="fe586-109">[in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe586-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="fe586-110">Return value</span></span>

<span data-ttu-id="fe586-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe586-111">S_OK</span></span> 
  
> <span data-ttu-id="fe586-112">La banque de messages a �t� correctement inform�e.</span><span class="sxs-lookup"><span data-stu-id="fe586-112">The message store was successfully notified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe586-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe586-113">Remarks</span></span>

<span data-ttu-id="fe586-114">La m�thode **IMsgStore::NotifyNewMail** est appel�e par le spouleur MAPI pour informer la banque de messages qu'un message est pr�t pour la livraison.</span><span class="sxs-lookup"><span data-stu-id="fe586-114">The **IMsgStore::NotifyNewMail** method is called by the MAPI spooler to inform the message store that a message is ready for delivery.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fe586-115">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="fe586-115">Notes to implementers</span></span>

<span data-ttu-id="fe586-p102">Lorsque **NotifyNewMail** est appel�, envoyer une notification de nouveau courrier � tous les clients inscrits. Vous pouvez envoyer la notification en appelant [IMAPISupport::Notify](imapisupport-notify.md), si vous choisissez d'utiliser les m�thodes de l'objet de prise en charge, ou � l'aide de votre propre impl�mentation. Un client enregistr� est celui qui a appel� [IMsgStore::Advise](imsgstore-advise.md) et d�finissez le param�tre  _lpEntryID_ NULL et le param�tre  _ulEventMask_ pour  _fnevNewMail_.</span><span class="sxs-lookup"><span data-stu-id="fe586-p102">When **NotifyNewMail** is called, send a new mail notification to all registered clients. You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation. A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_.</span></span> 
  
<span data-ttu-id="fe586-p103">Ne modifiez pas ou ne lib�rer de la m�moire pour la structure [NOTIFICATION](notification.md) qui d�crit la notification de nouveau courrier. Copiez la structure **NOTIFICATION** en appelant la fonction utilitaire [ScCopyNotifications](sccopynotifications.md) pour rendre utilisent les informations de ses membres.</span><span class="sxs-lookup"><span data-stu-id="fe586-p103">Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification. Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe586-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe586-121">See also</span></span>



[<span data-ttu-id="fe586-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="fe586-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="fe586-123">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="fe586-123">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
  
[<span data-ttu-id="fe586-124">Notification</span><span class="sxs-lookup"><span data-stu-id="fe586-124">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="fe586-125">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="fe586-125">ScCopyNotifications</span></span>](sccopynotifications.md)
  
[<span data-ttu-id="fe586-126">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fe586-126">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

