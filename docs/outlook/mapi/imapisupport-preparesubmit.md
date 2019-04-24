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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326319"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prépare un message à envoyer au spouleur MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> dans Pointeur vers le message à préparer.
    
 _lpulFlags_
  
> [in, out] Lors de l'entrée, le paramètre _lpulFlags_ est réservé et doit être égal à zéro. Lors de la sortie, _lpulFlags_ doit être null. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été correctement préparé.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::P reparesubmit** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages appellent **PrepareSubmit** dans leur implémentation de la méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) pour préparer un message à envoyer au spouleur MAPI. 
  
 **PrepareSubmit** est utilisé pour gérer les messages dont l'indicateur MSGFLAG_RESEND est défini dans leur propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND est défini pour les messages qui incluent une demande à renvoyer lorsqu'une transmission initiale échoue. **PrepareSubmit** détermine les destinataires de la liste de destinataires qui ont reçu le message et ceux qui ne l'ont pas été. 
  
Pour accéder à la liste des destinataires, **PrepareSubmit** appelle la méthode [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) du message. Pour récupérer les données du destinataire, **PrepareSubmit** appelle la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) de la table destinataire. Pour chaque ligne du tableau, **PrepareSubmit** vérifie la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) et effectue l'une des actions suivantes:
  
- Si l'indicateur MAPI_SUBMITTED est défini, **PrepareSubmit** efface l'indicateur et affecte la valeur false à la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)).
    
- Si l'indicateur MAPI_SUBMITTED n'est pas défini, **PrepareSubmit** modifie **PR_RECIPIENT_TYPE** en MAPI_P1 et définit **PR_RESPONSIBILITY** sur true. 
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Avant d'appeler **PrepareSubmit**, assurez-vous que vous avez appelé la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) et que vous avez défini l'indicateur NOTIFY_READYTOSEND dans le paramètre _ulFlags_ . L'appel **SpoolerNotify** doit être effectué une fois par session avant l'appel à **PrepareSubmit**. **SpoolerNotify** synchronise le spouleur MAPI et s'assure que tous les fournisseurs de transport nécessaires sont connectés et que leurs types d'adresses sont enregistrés. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

