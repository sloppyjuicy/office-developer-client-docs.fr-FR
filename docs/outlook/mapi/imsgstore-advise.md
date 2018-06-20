---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784235"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**S’applique à**: Outlook 
  
Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la banque de messages.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier ou du message sur les notifications doivent être générées, ou **valeur null**. Si _lpEntryID_ est défini sur NULL, **Advise** enregistre des notifications sur le magasin de l’intégralité du message. 
    
 _ulEventMask_
  
> [in] Un masque des valeurs qui indiquent les types d’événements de notification que l’appelant est intéressée par et doit être inclus dans l’enregistrement. Il existe une structure [NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui conserve des informations sur l’événement. Les valeurs valides pour le paramètre _ulEventMask_ sont les suivantes : 
    
 _fnevCriticalError_
  
> Enregistre les notifications sur les erreurs graves, telles que la mémoire insuffisante.
    
 _fnevExtended_
  
> Fournisseur de magasins registres pour les notifications concernant les événements spécifiques au message particulier.
    
 _fnevNewMail_
  
> Enregistre les notifications relatives à l’arrivée de nouveaux messages. 
    
 _fnevObjectCreated_
  
> Enregistre les notifications concernant la création d’un nouveau dossier ou un message.
    
 _fnevObjectCopied_
  
> Enregistre les notifications relatives à un dossier ou un message en cours de copie.
    
 _fnevObjectDeleted_
  
> Enregistre les notifications relatives à un dossier ou un message en cours de suppression.
    
 _fnevObjectModified_
  
> Enregistre les notifications relatives à un dossier ou un message en cours de modification.
    
 _fnevObjectMoved_
  
> Enregistre les notifications relatives à un dossier ou un message en cours de déplacement.
    
 _fnevSearchComplete_
  
> Enregistre les notifications relatives à la fin d’une opération de recherche.
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures. Cet objet de récepteur advise doit déjà affectée.
    
 _lpulConnection_
  
> [out] Un pointeur vers un nombre différent de zéro qui représente la connexion entre l’appelant de notification objet récepteur et la session. 
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures. Cet objet de récepteur advise doit déjà affectée. 
    
 _lpulConnection_
  
> [out] Objet récepteur et la banque de messages de notification un pointeur vers un numéro de connexion différente de zéro qui représente la connexion entre l’appelant.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’inscription a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de banque de messages ne gère pas l’inscription pour la notification par le biais de la banque de messages.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::Advise** établit une connexion entre l’appelant de notification de l’objet de réception et la banque de messages ou un objet dans la banque de messages. Cette connexion est utilisée pour envoyer des notifications pour le récepteur de notifications lorsqu’un ou plusieurs événements, tel que spécifié dans le paramètre _ulEventMask_ , se produisent sur l’objet source de notification. Lorsque le paramètre _lpEntryID_ pointe vers un identificateur d’entrée valide, la source advise est l’objet identifié par l’identificateur d’entrée. Lorsque _lpEntryID_ est NULL, la source advise est la banque de messages. 
  
Pour envoyer une notification, le fournisseur de banque de messages ou MAPI appelle méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur des notifications. L’un des paramètres à **OnNotify**, une structure de notification, contient des informations décrivant l’événement spécifique.
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous pouvez prendre en charge notification avec ou sans l’aide de MAPI. MAPI a trois méthodes d’objet de prise en charge pour aider les fournisseurs de services à implémenter la notification : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport::Notify](imapisupport-notify.md). Si vous choisissez d’utiliser les méthodes de prise en charge MAPI, appelé la méthode **Subscribe** lorsque votre méthode **Advise** est appelée et libérer le pointeur _lpAdviseSink_ . 
  
Si vous choisissez prendre en charge de notification vous-même, appelez la méthode de [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) du récepteur advise représenté par le paramètre _lpAdviseSink_ de conserver une copie de ce pointeur. Mettre à jour cette copie jusqu'à ce que votre méthode [IMsgStore::Unadvise](imsgstore-unadvise.md) est appelée pour annuler l’inscription. 
  
Quelle que soit la façon dont vous prenez en charge la notification, affecter un numéro de connexion différente de zéro pour l’inscription de notification et la faire revenir dans le paramètre _lpulConnection_ . Ne relâchez pas ce numéro de connexion jusqu'à ce que **Unadvise** a été appelée et terminé. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut également se produire sur n’importe quel thread à tout moment. Si vous devez être assuré que les notifications se produisent uniquement à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet récepteur advise que vous passez à **Advise**. 
  
Après un appel **Advise** a réussi et **Unadvise** a été appelé pour annuler l’enregistrement, avant d’être préparé pour l’objet de récepteur advise doit être publié. Vous devez libérer votre objet de récepteur advise après **Advise** renvoie à moins d’avoir une utilisation à long terme spécifique pour qu’il. 
  
Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur la gestion des notifications, voir [Gestion des Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI utilise la méthode **IMsgStore::Advise** pour enregistrer les notifications dans le magasin de l’intégralité du message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notification](notification.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

