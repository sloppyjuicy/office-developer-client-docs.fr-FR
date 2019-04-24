---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317149"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise un nouveau message.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Paramètres

 _pMessageSite_
  
> dans Pointeur vers le site de messagerie que le formulaire utilisera pour fonctionner avec le message dans la visionneuse.
    
 _pMessage_
  
> dans Pointeur vers le nouveau message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau message a été initialisé.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IPersistMessage:: InitNew** lorsque l'utilisateur écrit un nouveau message qui appartient à une classe de message gérée par le formulaire. Si l'objet Form est doté d'un pointeur d'interface utilisateur valide, l'interface utilisateur de l'objet message doit être affichée. 
  
 **InitNew** ne doit pas être appelé lorsque l'état de votre formulaire est différent de l'état [non initialisé](uninitialized-state.md) . Si le formulaire est dans l'un des autres États lorsque **InitNew** est appelé, renvoyer E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

En règle générale, les messages dont les propriétés ne sont pas enregistrées sont marqués comme étant modifiés afin que le client puisse afficher une boîte de dialogue qui invite l'utilisateur à indiquer si ces propriétés doivent être enregistrées. Si l'utilisateur indique qu'un message doit être enregistré, enregistrez les données, marquez le message comme nettoyé, puis quittez normalement.
  
Toutefois, si le traitement de vos messages nouvellement initialisés inclut la définition d'une ou de plusieurs propriétés calculées et qu'il est important que ces propriétés soient enregistrées, ne Marquez pas les messages comme étant modifiés. Étant donné que les propriétés calculées doivent être invisibles pour les utilisateurs, aucune boîte de dialogue ne doit s'afficher.
  
Si votre formulaire comporte une référence à un site de messagerie actif autre que celui qui est transmis à **InitNew**, libérez le site d'origine car il ne sera plus utilisé. Stockez les pointeurs sur le site de messagerie et le message des paramètres _pMessageSite_ et _pMessage_ et appelez les deux méthodes « [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) » pour incrémenter leur nombre de références. 
  
Définissez les propriétés **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) et **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour le nouveau message à une valeur appropriée pour votre classe de message. De nombreuses classes de message, par exemple, Set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for New messages. 
  
Avant de retourner, faire basculer le formulaire vers l'état [normal](normal-state.md) si aucune erreur n'est survenue. Envoyez une nouvelle notification par message à toutes les visionneuses inscrites en appelant leurs méthodes [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) et en retournant S_OK. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Une fois que vous avez effectué un appel réussi à **InitNew**, vous pouvez supposer que les propriétés requises suivantes, et aucune autre, ont été définies pour le formulaire:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Pour plus d'informations sur les États de formulaires, voir [États de formulaire](form-states.md). Pour plus d'informations sur la façon dont les objets de stockage sont initialisés, consultez la méthode [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

