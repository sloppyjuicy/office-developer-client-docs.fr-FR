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
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**S’applique à**: Outlook 
  
Récupère l’objet sous-jacent [IMessage : IMAPIProp](imessageimapiprop.md) que ce [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) est encapsulation. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Paramètres

 _ppmsg_
  
> [out] Un objet de message sécurisé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

