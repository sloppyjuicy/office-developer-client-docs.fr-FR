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
  
Informe le fournisseur de transport que lepooler MAPI a terminé son traitement sur un message sortant.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulMsgRef_
  
> [in] Valeur de référence spécifique au message obtenue lors d’un appel précédent à la méthode [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) 
    
 _lpulFlags_
  
> [out] Masque de bits d’indicateurs qui indique aupooler MAPI ce qu’il doit faire avec le message. Si aucun indicateur n’est définie, le message a été envoyé. Les indicateurs suivants peuvent être définies :
    
END_DONT_RESEND 
  
> Pour l’instant, le fournisseur de transport dispose de toutes les informations nécessaires sur ce message. Lorsque le fournisseur de transport requiert plus d’informations ou lorsqu’il a envoyé le message, il avertit lepooler MAPI en appelant la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’indicateur NOTIFY_SENTDEFERRED et en passant l’identificateur d’entrée du message. 
    
END_RESEND_LATER 
  
> Le fournisseur de transport n’envoie pas le message pour le moment pour des raisons qui ne sont pas des conditions d’erreur. Le fournisseur de transport doit être appelé à nouveau ultérieurement pour envoyer le message.
    
END_RESEND_NOW 
  
> Le fournisseur de transport doit redémarrer le message qui lui a été transmis dans un appel de méthode [IMessage::SubmitMessage.](imessage-submitmessage.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::EndMessage** après avoir terminé le traitement impliqué dans la fourniture d’informations de remise étendues ou de non remise. 
  
Une fois que cet appel est revenu, la valeur dans le  _paramètre ulMsgRef_ n’est plus valide pour ce message. Le fournisseur de transport peut réutiliser la même valeur sur un message futur. 
  
Tous les objets que le fournisseur de transport ouvre lors du transfert d’un message doivent être libérés avant le retour de l’appel **EndMessage,** à l’exception de l’objet message que lepooler MAPI transmet au fournisseur de transport. L’objet message transmis par lepooler MAPI n’est pas valide après **l’appel EndMessage.** 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

