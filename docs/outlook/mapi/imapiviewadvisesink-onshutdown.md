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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2a09731dbd0ba2c5d6c1055a7c5ed11097c5ef27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784108"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="e574c-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="e574c-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="e574c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e574c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e574c-105">Avertit la visionneuse de formulaire fermeture d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="e574c-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="e574c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e574c-106">Parameters</span></span>

<span data-ttu-id="e574c-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="e574c-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e574c-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e574c-108">Return value</span></span>

<span data-ttu-id="e574c-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="e574c-109">S_OK</span></span> 
  
> <span data-ttu-id="e574c-110">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="e574c-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e574c-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e574c-111">Remarks</span></span>

<span data-ttu-id="e574c-112">Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="e574c-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e574c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e574c-113">See also</span></span>



[<span data-ttu-id="e574c-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e574c-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

