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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394880"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise un nouveau message.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Paramètres

 _pMessageSite_
  
> [in] Pointeur vers le site de message qui sera utilisée pour travailler avec le message dans la visionneuse.
    
 _pMessage_
  
> [in] Pointeur vers le nouveau message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nouveau message a été correctement initialisé.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IPersistMessage::InitNew** lorsque l’utilisateur écrit un nouveau message qui appartient à une classe de message qui gère le formulaire. Si l’objet form possède un pointeur d’interface utilisateur valide, l’interface utilisateur pour l’objet du message doit être affichée. 
  
 **InitNew** ne doit pas être appelée lorsque le formulaire est dans un état à l’exception de l’état [Uninitialized](uninitialized-state.md) . Si le formulaire est dans un des autres États lorsque **InitNew** est appelée, retourner E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

En règle générale, les messages qui contiennent des propriétés non enregistrées sont marquées comme modifiées afin que le client peut afficher une boîte de dialogue qui demande à l’utilisateur si ces propriétés doivent être enregistrées. Si l’utilisateur indique qu’un message doit être enregistré, enregistrer les données, marquer le message en tant que nouvelle et quitter normalement.
  
Toutefois, si le traitement de vos messages initialisés récemment inclut la définition d’une ou plusieurs des propriétés calculées et il est important pour les propriétés à être enregistrée, ne marquez pas les messages modifié. Calculée propriétés doivent être invisibles pour les utilisateurs, aucune boîte de dialogue ne doit affiché.
  
Si votre formulaire comporte une référence à un site de message actif différent de celui qui est passée dans **InitNew**, version du site d’origine, car il sera ne plus être utilisé. Stocker des pointeurs vers le site de message et le message à partir des paramètres _pMessageSite_ et _pMessage_ et appelez des deux objets [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) pour incrémenter son décompte de références. 
  
Définir les propriétés de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour le nouveau message et le **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) par un nom approprié pour votre classe de message. De nombreuses classes de message, par exemple, définissent **PR_MESSAGE_FLAGS** à MSGFLAG_UNSENT pour les nouveaux messages. 
  
Avant de retourner, transition du formulaire à l’état [Normal](normal-state.md) si aucune erreur ne se sont produites. Envoyer une notification de nouveau message à tous les utilisateurs inscrits en appelant les méthodes [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) et qu’elles retournent S_OK. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Après avoir apporté **InitNew**un appel réussi, vous pouvez supposer que les propriétés requises suivantes et aucune autre, ont été définies pour le formulaire :
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Pour plus d’informations sur les États de formulaires, voir [États du formulaire](form-states.md). Pour plus d’informations sur l’initialisation des objets de stockage, voir la méthode [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

