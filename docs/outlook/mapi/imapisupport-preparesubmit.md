---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
ms.openlocfilehash: 35b6ac323981fa1a0a4db7b424ff480307aa04af
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374396"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

**S’applique à** : Outlook 2013 | Outlook 2016

Prépare un message à envoyer aupooler MAPI.

```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_

> [in] Pointeur vers le message à préparer.

 _lpulFlags_

> [in, out] En entrée, le _paramètre lpulFlags_ est réservé et doit être zéro. En sortie, _lpulFlags doit_ avoir la valeur NULL.

## <a name="return-value"></a>Valeur renvoyée

S_OK

> Le message a été correctement préparé.

## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::P repareSubmit** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages appellent **PrepareSubmit** dans leur implémentation de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour préparer un message à envoyer aupooler MAPI.

 **PrepareSubmit** est utilisé pour gérer les messages dont l’indicateur MSGFLAG_RESEND est définie dans leur propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND est définie pour les messages qui incluent une demande à envoyer en cas d’échec de la transmission initiale. **PrepareSubmit** détermine lequel des destinataires de la liste des destinataires a reçu le message avec succès et qui ne l’a pas été.

Pour accéder à la liste des **destinataires, PrepareSubmit** appelle la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message. Pour récupérer les données du destinataire, **PrepareSubmit** appelle la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de la table des destinataires. Pour chaque ligne du tableau, **PrepareSubmit** vérifie la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) et prend l’une des actions suivantes :

- Si l MAPI_SUBMITTED est définie, **PrepareSubmit** l’effacera et définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) sur FALSE.

- Si l’MAPI_SUBMITTED n’est pas définie, **PrepareSubmit** **PR_RECIPIENT_TYPE à MAPI_P1** et définit **PR_RESPONSIBILITY sur TRUE** .

## <a name="notes-to-callers"></a>Remarques pour les appelants

Avant d’appeler **PrepareSubmit**, assurez-vous d’avoir appelé la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) et définissez l’indicateur NOTIFY_READYTOSEND dans le paramètre _ulFlags_ . **L’appel SpoolerNotify** doit être effectué une fois par session avant l’appel **à PrepareSubmit**. **SpoolerNotify** synchronise lepooler MAPI et garantit que tous les fournisseurs de transport nécessaires sont connectés et que leurs types d’adresses sont enregistrés.
 
## <a name="see-also"></a>Voir aussi

[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)  
[IMessage::SubmitMessage](imessage-submitmessage.md)  
[IMAPISupport : IUnknown](imapisupportiunknown.md)
