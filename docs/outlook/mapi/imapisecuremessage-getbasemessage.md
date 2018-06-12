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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783912"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="b55e1-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="b55e1-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="b55e1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b55e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b55e1-105">Récupère l’objet sous-jacent [IMessage : IMAPIProp](imessageimapiprop.md) que ce [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) est encapsulation.</span><span class="sxs-lookup"><span data-stu-id="b55e1-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="b55e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b55e1-106">Parameters</span></span>

 <span data-ttu-id="b55e1-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="b55e1-107">_ppmsg_</span></span>
  
> <span data-ttu-id="b55e1-108">[out] Un objet de message sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b55e1-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b55e1-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b55e1-109">Return value</span></span>

<span data-ttu-id="b55e1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b55e1-110">S_OK</span></span>
  
> <span data-ttu-id="b55e1-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b55e1-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b55e1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b55e1-112">See also</span></span>



[<span data-ttu-id="b55e1-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b55e1-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="b55e1-114">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b55e1-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

