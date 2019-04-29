---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419603"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaires qu'un nouveau message ou un message existant a été chargé dans un formulaire.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewAdviseSink:: OnNewMessage** chaque fois qu'un message est chargé dans un formulaire à l'aide de la méthode [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) . 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Libérez votre pointeur actif sur l'objet de formulaire, car il ne pointe plus vers le message que votre visionneuse était précédemment en train d'afficher. 
  
Pour plus d'informations sur les notifications de formulaire, consultez la rubrique [envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

