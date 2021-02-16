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
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428577"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="9ede5-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="9ede5-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="9ede5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ede5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ede5-105">Extrait [l’IMessage sous-jacent : IMAPIProp](imessageimapiprop.md) que ce [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) encapsule.</span><span class="sxs-lookup"><span data-stu-id="9ede5-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="9ede5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ede5-106">Parameters</span></span>

 <span data-ttu-id="9ede5-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="9ede5-107">_ppmsg_</span></span>
  
> <span data-ttu-id="9ede5-108">[out] Objet de message sécurisé.</span><span class="sxs-lookup"><span data-stu-id="9ede5-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9ede5-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ede5-109">Return value</span></span>

<span data-ttu-id="9ede5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ede5-110">S_OK</span></span>
  
> <span data-ttu-id="9ede5-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="9ede5-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ede5-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ede5-112">See also</span></span>



[<span data-ttu-id="9ede5-113">IMAPISecureMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ede5-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="9ede5-114">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9ede5-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

