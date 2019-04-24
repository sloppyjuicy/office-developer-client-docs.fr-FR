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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322392"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="23105-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="23105-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="23105-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23105-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23105-105">Récupère le [IMessage: IMAPIProp](imessageimapiprop.md) sous-jacent que cette [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) est en encapsulation.</span><span class="sxs-lookup"><span data-stu-id="23105-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="23105-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23105-106">Parameters</span></span>

 <span data-ttu-id="23105-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="23105-107">_ppmsg_</span></span>
  
> <span data-ttu-id="23105-108">remarquer Objet de message sécurisé.</span><span class="sxs-lookup"><span data-stu-id="23105-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23105-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23105-109">Return value</span></span>

<span data-ttu-id="23105-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="23105-110">S_OK</span></span>
  
> <span data-ttu-id="23105-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="23105-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23105-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23105-112">See also</span></span>



[<span data-ttu-id="23105-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23105-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="23105-114">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="23105-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

