---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5f45a6457bba738b290d967260bbd34c0f88f93f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595061"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Il prépare un message pour son envoi au spouleur MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> [in] Pointeur vers le message préparer.
    
 _lpulFlags_
  
> [entrée, sortie] À l’entrée, le paramètre _lpulFlags_ est réservé et doit être égal à zéro. Dans la sortie, _lpulFlags_ doit être NULL. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le message a été correctement préparé.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::PrepareSubmit** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de banque de messages appeler **PrepareSubmit** dans leur implémentation de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour préparer un message pour son envoi au spouleur MAPI. 
  
 **PrepareSubmit** est utilisé pour gérer les messages dont l’indicateur MSGFLAG_RESEND dans leur propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND est définie pour les messages qui incluent une demande à être renvoyées en cas d’échec d’une transmission initiale. **PrepareSubmit** détermine parmi les destinataires dans la liste des destinataires a reçu le message et qui ont échoué. 
  
Pour accéder à la liste des destinataires, **PrepareSubmit** appelle la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message. Pour récupérer les données du destinataire, **PrepareSubmit** appelle la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de destinataire de la table. Pour chaque ligne dans le tableau, **PrepareSubmit** vérifie la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) et peut prendre l’une des actions suivantes :
  
- Si l’indicateur MAPI_SUBMITTED est défini, **PrepareSubmit** efface l’indicateur et définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) sur FALSE.
    
- Si l’indicateur MAPI_SUBMITTED n’est pas définie, **PrepareSubmit** devient **PR_RECIPIENT_TYPE** MAPI_P1 et définit **PR_RESPONSIBILITY** sur TRUE. 
    
## <a name="notes-to-callers"></a>Notes aux appelants

Avant d’appeler **PrepareSubmit**, n’oubliez pas que vous avez appelé la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) et définissez l’indicateur NOTIFY_READYTOSEND dans le paramètre _ulFlags_ . L’appel **SpoolerNotify** doit être effectuée qu’une seule fois par session avant l’appel à **PrepareSubmit**. **SpoolerNotify** synchronise le spouleur MAPI et garantit que tous les fournisseurs de transport nécessaires sont connectés et leurs types d’adresses sont enregistrées. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

