---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f49ea23ed7fef91bcb360483611af2ee60429934
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592968"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="bdcc0-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="bdcc0-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="bdcc0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdcc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdcc0-105">Avertit la visionneuse de formulaire fermeture d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="bdcc0-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="bdcc0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdcc0-106">Parameters</span></span>

<span data-ttu-id="bdcc0-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="bdcc0-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="bdcc0-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bdcc0-108">Return value</span></span>

<span data-ttu-id="bdcc0-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="bdcc0-109">S_OK</span></span> 
  
> <span data-ttu-id="bdcc0-110">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="bdcc0-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bdcc0-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="bdcc0-111">Remarks</span></span>

<span data-ttu-id="bdcc0-112">Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="bdcc0-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bdcc0-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdcc0-113">See also</span></span>



[<span data-ttu-id="bdcc0-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdcc0-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

