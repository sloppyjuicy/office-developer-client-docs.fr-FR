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
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317324"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
S'inscrire pour recevoir une notification des événements spécifiés qui affectent la Banque de messages.
  
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du dossier ou du message sur les notifications à générer, ou sur **null**. Si _lpEntryID_ est défini sur null, **Advise** les registres des notifications sur l'intégralité de la Banque de messages. 
    
 _ulEventMask_
  
> dans Masque de valeurs qui indiquent les types d'événements de notification qui intéressent l'appelant et qui doit être inclus dans l'inscription. Il existe une structure de [notification](notification.md) correspondante associée à chaque type d'événement qui contient des informations sur l'événement. Les valeurs valides pour le paramètre _ulEventMask_ sont les suivantes: 
    
 _fnevCriticalError_
  
> Enregistre les notifications concernant les erreurs graves, telles que la mémoire insuffisante.
    
 _fnevExtended_
  
> Enregistre les notifications relatives aux événements spécifiques au fournisseur de banque de messages particulier.
    
 _fnevNewMail_
  
> Enregistre les notifications relatives à l'arrivée de nouveaux messages. 
    
 _fnevObjectCreated_
  
> Enregistre les notifications relatives à la création d'un nouveau dossier ou d'un nouveau message.
    
 _fnevObjectCopied_
  
> Enregistre les notifications relatives à la copie d'un dossier ou d'un message.
    
 _fnevObjectDeleted_
  
> Enregistre les notifications relatives à la suppression d'un dossier ou d'un message.
    
 _fnevObjectModified_
  
> Enregistre les notifications relatives à la modification d'un dossier ou d'un message.
    
 _fnevObjectMoved_
  
> Enregistre les notifications relatives à un dossier ou à un message déplacé.
    
 _fnevSearchComplete_
  
> Enregistre les notifications relatives à l'exécution d'une opération de recherche.
    
 _lpAdviseSink_
  
> dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes. Cet objet de récepteur de notifications doit déjà avoir été alloué.
    
 _lpulConnection_
  
> remarquer Pointeur vers un nombre différent de zéro qui représente la connexion entre l'objet de récepteur d'avertissement de l'appelant et la session. 
    
 _lpAdviseSink_
  
> dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes. Cet objet de récepteur de notifications doit déjà avoir été alloué. 
    
 _lpulConnection_
  
> remarquer Pointeur vers un numéro de connexion différent de zéro qui représente la connexion entre l'objet de récepteur de notification de l'appelant et la Banque de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'inscription a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de banque de messages ne prend pas en charge l'enregistrement des notifications par le biais de la Banque de messages.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: Advise** établit une connexion entre l'objet récepteur de notification de l'appelant et la Banque de messages ou un objet dans la Banque de messages. Cette connexion est utilisée pour envoyer des notifications au récepteur de notifications lorsqu'un ou plusieurs événements, tels que spécifiés dans le paramètre _ulEventMask_ , ont lieu dans l'objet de source Advise. Lorsque le paramètre _lpEntryID_ pointe vers un identificateur d'entrée valide, la source de notification est l'objet identifié par cet identificateur d'entrée. Lorsque _lpEntryID_ est null, la source de notification est la Banque de messages. 
  
Pour envoyer une notification, le fournisseur de banque de messages ou MAPI appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de notification enregistré. L'un des paramètres de **OnNotify**, une structure de notification, contient des informations qui décrivent l'événement spécifique.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez prendre en charge les notifications avec ou sans l'aide de MAPI. MAPI dispose de trois méthodes d'objet de prise en charge pour aider les fournisseurs de services à implémenter la notification: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport:: Notify](imapisupport-notify.md). Si vous choisissez d'utiliser les méthodes de prise en charge MAPI, appelez **subscribe** lorsque votre méthode Advise est appelée et relâchez le pointeur _lpAdviseSink_ . **** 
  
Si vous choisissez de prendre en charge la notification vous-même, appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du récepteur de notifications représenté par le paramètre _lpAdviseSink_ pour conserver une copie de ce pointeur. Conservez cette copie jusqu'à ce que la méthode [IMsgStore::](imsgstore-unadvise.md) Unadvise soit appelée pour annuler l'inscription. 
  
Quelle que soit la façon dont vous prenez en charge la notification, attribuez un numéro de connexion différent de zéro à l'enregistrement des notifications et renvoyez-le dans le paramètre _lpulConnection_ . Ne libérez pas ce numéro de **** connexion tant que Unadvise n'a pas été appelé et qu'il est terminé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut également se produire sur n'importe quel thread à tout moment. Si vous devez être sûr que les notifications ne se produisent qu'à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l'objet de récepteur de notifications que vous transmettez à l' **avis**. 
  
Une fois qu'un **** appel à Advise a réussi et avant que Unadvise ait été appelé pour annuler l'inscription, soyez prêt à libérer l'objet de récepteur de notifications. **** Vous devez libérer votre objet de récepteur d' **** avertissement après le renvoi de la fonction Advise, sauf si vous disposez d'une utilisation de longue durée spécifique. 
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). 
  
Pour plus d'informations sur la gestion des notifications, consultez la rubrique [gestion](handling-notifications.md)des notifications. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnNotificationsOn  <br/> |MFCMAPI utilise la méthode **IMsgStore:: Advise** pour s'inscrire aux notifications sur l'intégralité de la Banque de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notification](notification.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

