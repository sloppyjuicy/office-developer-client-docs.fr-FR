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
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère l’objet sous-jacent [IMessage : IMAPIProp](imessageimapiprop.md) que ce [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) est encapsulation. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Paramètres

 _ppmsg_
  
> [out] Un objet de message sécurisé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

