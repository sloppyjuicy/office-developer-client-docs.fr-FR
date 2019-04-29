---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414157"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informe le fournisseur de transport que le spouleur MAPI a terminé son traitement sur un message sortant.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulMsgRef_
  
> dans Une valeur de référence spécifique à un message qui a été obtenue lors d'un appel précédent à la méthode [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) . 
    
 _lpulFlags_
  
> remarquer Masque de réindicateur des indicateurs qui indique au spouleur MAPI ce qu'il doit faire avec le message. Si aucun indicateur n'est défini, le message a été envoyé. Les indicateurs suivants peuvent être définis:
    
END_DONT_RESEND 
  
> Le fournisseur de transport dispose de toutes les informations nécessaires sur ce message pour le moment. Lorsque le fournisseur de transport demande davantage d'informations ou lorsqu'il a envoyé le message, il avertit le spouleur MAPI en appelant la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) avec l'indicateur NOTIFY_SENTDEFERRED et en transmettant l'identificateur d'entrée du message. 
    
END_RESEND_LATER 
  
> Le fournisseur de transport n'envoie pas le message à l'heure actuelle pour les raisons qui ne sont pas des erreurs. Le fournisseur de transport doit être appelé à nouveau ultérieurement pour envoyer le message.
    
END_RESEND_NOW 
  
> Le fournisseur de transport doit redémarrer le message qui lui a été transmis dans un appel de méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon:: EndMessage** une fois qu'il a terminé le traitement impliqué dans la fourniture d'informations de remise étendue ou de non-remise. 
  
Une fois cet appel retourné, la valeur du paramètre _ulMsgRef_ n'est plus valide pour ce message. Le fournisseur de transport peut réutiliser la même valeur sur un message ultérieur. 
  
Tous les objets que le fournisseur de transport ouvre pendant le transfert d'un message doivent être libérés avant le renvoi de l'appel **EndMessage** , à l'exception de l'objet message que le spouleur MAPI transmet au fournisseur de transport. L'objet message transmis par le spouleur MAPI n'est pas valide après l'appel **EndMessage** . 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

