---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
ms.openlocfilehash: cb455858fec9020c558958282e8066d3250e256b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370658"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait [l’IMessage sous-jacent : IMAPIProp](imessageimapiprop.md) que ce [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) encapsule. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Paramètres

 _ppmsg_
  
> [out] Objet de message sécurisé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

