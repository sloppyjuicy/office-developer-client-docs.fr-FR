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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: adf9b28e941e9ead9b83660f58701f13f35cabc7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784120"
---
# <a name="imapiviewadvisesinkonnewmessage"></a><span data-ttu-id="6c7f7-103">IMAPIViewAdviseSink::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="6c7f7-103">IMAPIViewAdviseSink::OnNewMessage</span></span>

  
  
<span data-ttu-id="6c7f7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c7f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c7f7-105">Indique la visionneuse de formulaire à une nouvelle ou un message existant a été chargé dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-105">Notifies the form viewer that a new or an existing message has been loaded in a form.</span></span>
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="6c7f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c7f7-106">Parameters</span></span>

<span data-ttu-id="6c7f7-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="6c7f7-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6c7f7-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6c7f7-108">Return value</span></span>

<span data-ttu-id="6c7f7-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c7f7-109">S_OK</span></span> 
  
> <span data-ttu-id="6c7f7-110">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c7f7-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c7f7-111">Remarks</span></span>

<span data-ttu-id="6c7f7-112">Objets de formulaire appeler la méthode de **IMAPIViewAdviseSink::OnNewMessage** lorsqu’un message est chargé dans un formulaire à l’aide de la méthode le [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) .</span><span class="sxs-lookup"><span data-stu-id="6c7f7-112">Form objects call the **IMAPIViewAdviseSink::OnNewMessage** method whenever a message is loaded in a form using either the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6c7f7-113">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="6c7f7-113">Notes to implementers</span></span>

<span data-ttu-id="6c7f7-114">Libérer le pointeur actif à l’objet de formulaire, car il ne pointe plus vers le message que votre Observateur a été précédemment affichage.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-114">Release your active pointer to the form object because it no longer points to the message your viewer was formerly viewing.</span></span> 
  
<span data-ttu-id="6c7f7-115">Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6c7f7-115">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c7f7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c7f7-116">See also</span></span>



[<span data-ttu-id="6c7f7-117">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c7f7-117">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)
  
[<span data-ttu-id="6c7f7-118">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="6c7f7-118">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="6c7f7-119">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="6c7f7-119">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="6c7f7-120">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c7f7-120">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

