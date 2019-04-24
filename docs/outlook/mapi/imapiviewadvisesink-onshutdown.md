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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b43c1b96130052a05ac390f10f545a66fe72b7fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351162"
---
# <a name="imapiviewadvisesinkonshutdown"></a><span data-ttu-id="bb9bb-103">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="bb9bb-103">IMAPIViewAdviseSink::OnShutdown</span></span>

  
  
<span data-ttu-id="bb9bb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb9bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb9bb-105">Avertit la visionneuse de formulaires qu'un formulaire est en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="bb9bb-105">Notifies the form viewer that a form is being closed.</span></span>
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a><span data-ttu-id="bb9bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb9bb-106">Parameters</span></span>

<span data-ttu-id="bb9bb-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="bb9bb-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="bb9bb-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb9bb-108">Return value</span></span>

<span data-ttu-id="bb9bb-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb9bb-109">S_OK</span></span> 
  
> <span data-ttu-id="bb9bb-110">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="bb9bb-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb9bb-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb9bb-111">Remarks</span></span>

<span data-ttu-id="bb9bb-112">Pour plus d'informations sur les notifications de formulaire, consultez la rubrique [envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="bb9bb-112">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb9bb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb9bb-113">See also</span></span>



[<span data-ttu-id="bb9bb-114">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb9bb-114">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

