---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: de450ddef3990f788f3e92ac39b15345aa3adf62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630564"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaire qu’un nouveau message ou un message existant a été chargé dans un formulaire.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Les objets form appellent la méthode **IMAPIViewAdviseSink::OnNewMessage** chaque fois qu’un message est chargé dans un formulaire à l’aide de la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load.](ipersistmessage-load.md) 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Relâchez votre pointeur actif vers l’objet formulaire, car il ne pointe plus vers le message que votre visionneuse visionnait auparavant. 
  
Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

