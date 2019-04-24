---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328790"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="32625-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="32625-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="32625-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32625-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32625-105">Avertit la visionneuse de formulaires qu'un nouveau message ou un message existant a été chargé dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="32625-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="32625-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32625-106">Parameters</span></span>

<span data-ttu-id="32625-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="32625-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="32625-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="32625-108">Return value</span></span>

<span data-ttu-id="32625-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="32625-109">S_OK</span></span> 
  
> <span data-ttu-id="32625-110">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="32625-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32625-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="32625-111">Remarks</span></span>

<span data-ttu-id="32625-112">Les objets de formulaire appellent la méthode **IMAPIViewAdviseSink:: OnNewMessage** chaque fois qu'un message est chargé dans un formulaire à l'aide de la méthode [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="32625-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="32625-113">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="32625-113">Notes to implementers</span></span>

<span data-ttu-id="32625-114">Libérez votre pointeur actif sur l'objet de formulaire, car il ne pointe plus vers le message que votre visionneuse était précédemment en train d'afficher.</span><span class="sxs-lookup"><span data-stu-id="32625-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="32625-115">Pour plus d'informations sur les notifications de formulaire, consultez la rubrique [envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="32625-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32625-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32625-116">See also</span></span>



[<span data-ttu-id="32625-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32625-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="32625-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="32625-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="32625-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="32625-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="32625-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32625-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

