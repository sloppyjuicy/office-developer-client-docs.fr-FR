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
ms.openlocfilehash: bb373e4b666f44c432ac1b04c0449eb7f0408a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592933"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique la visionneuse de formulaire à une nouvelle ou un message existant a été chargé dans un formulaire.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Paramètres

Aucune
  
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode de **IMAPIViewAdviseSink::OnNewMessage** lorsqu’un message est chargé dans un formulaire à l’aide de la méthode le [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Libérer le pointeur actif à l’objet de formulaire, car il ne pointe plus vers le message que votre Observateur a été précédemment affichage. 
  
Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

