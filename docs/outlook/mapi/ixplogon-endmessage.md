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
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582468"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informe le fournisseur de transport que le spouleur MAPI terminé son traitement d’un message sortant.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulMsgRef_
  
> [in] Une valeur de référence de message spécifique qui a été obtenue dans un appel précédent à la méthode [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . 
    
 _lpulFlags_
  
> [out] Masque de bits d’indicateurs qui indique au spouleur MAPI quoi faire avec le message. Si aucun indicateur est défini, le message a été envoyé. Les indicateurs suivants peuvent être définis :
    
END_DONT_RESEND 
  
> Le fournisseur de transport a toutes les informations nécessaires sur ce message pour l’instant. Lorsque le fournisseur de transport nécessite plus d’informations ou lorsqu’il a envoyé le message, il notifie le spouleur MAPI en appelant la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’indicateur NOTIFY_SENTDEFERRED et en transmettant l’identificateur d’entrée du message. 
    
END_RESEND_LATER 
  
> Le fournisseur de transport n’envoie pas le message à l’heure actuelle pour des raisons qui ne sont pas des conditions d’erreur. Le fournisseur de transport doit être appelé à nouveau ultérieurement pour envoyer le message.
    
END_RESEND_NOW 
  
> Le fournisseur de transport doit redémarrer le message passé dans un appel de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::EndMessage** une fois le traitement entrent en jeu dans remise étendue ou les informations de non-remise. 
  
Une fois que cet appel retourne la valeur dans le paramètre _ulMsgRef_ n’est plus valide pour ce message. Le fournisseur de transport peut réutiliser la même valeur d’un message de futur. 
  
Tous les objets qui le fournisseur de transport s’ouvre lors du transfert d’un message doivent être libérés avant le retour **EndMessage** , à l’exception de l’objet de message le spouleur MAPI transmet au fournisseur de transport. L’objet du message sont transmise par le spouleur MAPI n’est pas valide après l’appel de **EndMessage** . 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

