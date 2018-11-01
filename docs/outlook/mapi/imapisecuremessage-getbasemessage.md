---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d246fc0cfc60d0a2b9ff12ee70eae2366cf9b53a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594837"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="59c5c-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="59c5c-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="59c5c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59c5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59c5c-105">Récupère l’objet sous-jacent [IMessage : IMAPIProp](imessageimapiprop.md) que ce [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) est encapsulation.</span><span class="sxs-lookup"><span data-stu-id="59c5c-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="59c5c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59c5c-106">Parameters</span></span>

 <span data-ttu-id="59c5c-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="59c5c-107">_ppmsg_</span></span>
  
> <span data-ttu-id="59c5c-108">[out] Un objet de message sécurisé.</span><span class="sxs-lookup"><span data-stu-id="59c5c-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59c5c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="59c5c-109">Return value</span></span>

<span data-ttu-id="59c5c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="59c5c-110">S_OK</span></span>
  
> <span data-ttu-id="59c5c-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="59c5c-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59c5c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c5c-112">See also</span></span>



[<span data-ttu-id="59c5c-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59c5c-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="59c5c-114">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="59c5c-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

