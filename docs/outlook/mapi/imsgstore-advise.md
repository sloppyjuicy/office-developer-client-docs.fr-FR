---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1f9a32cf295c1df0de2795bb75085ed168ec5399
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462903"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
S’inscrit pour recevoir une notification des événements spécifiés qui affectent la boutique de messages.
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier ou du message sur les notifications à générer, ou **null**. Si  _lpEntryID_ est définie sur NULL, **Advise** s’inscrit pour les notifications sur l’ensemble de la boutique de messages. 
    
 _ulEventMask_
  
> [in] Masque de valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et qui doivent être inclus dans l’inscription. Il existe une structure [de NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui contient des informations sur l’événement. Les valeurs suivantes sont valides pour  _le paramètre ulEventMask_ : 
    
 _fnevCriticalError_
  
> S’inscrit aux notifications concernant les erreurs graves, telles que la mémoire insuffisante.
    
 _fnevExtended_
  
> S’inscrit pour les notifications sur les événements spécifiques au fournisseur de magasin de messages particulier.
    
 _fnevNewMail_
  
> S’inscrit aux notifications concernant l’arrivée de nouveaux messages. 
    
 _fnevObjectCreated_
  
> S’inscrit aux notifications concernant la création d’un dossier ou d’un message.
    
 _fnevObjectCopied_
  
> S’inscrit aux notifications concernant un dossier ou un message en cours de copie.
    
 _fnevObjectDeleted_
  
> S’inscrit aux notifications concernant la suppression d’un dossier ou d’un message.
    
 _fnevObjectModified_
  
> S’inscrit aux notifications concernant la modification d’un dossier ou d’un message.
    
 _fnevObjectMoved_
  
> S’inscrit aux notifications concernant un dossier ou un message déplacé.
    
 _fnevSearchComplete_
  
> S’inscrit aux notifications concernant la fin d’une opération de recherche.
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes. Cet objet de sink de conseil doit avoir déjà été alloué.
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro autre que zéro qui représente la connexion entre l’objet de l’objet de conseiller de l’appelant et la session. 
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes. Cet objet de sink de conseil doit avoir déjà été alloué. 
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro de connexion autre que zéro qui représente la connexion entre l’objet de l’objet de conseiller de l’appelant et la magasin de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de la boutique de messages ne prend pas en charge l’inscription pour la notification via la boutique de messages.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::Advise** établit une connexion entre l’objet de l’objet de l’appelant qui le conseille et la magasin de messages ou un objet dans la magasin de messages. Cette connexion est utilisée pour envoyer des notifications au réception de notification lorsqu’un ou plusieurs événements, comme spécifié dans le paramètre _ulEventMask_ , se produisent à l’objet source de notification. Lorsque le  _paramètre lpEntryID_ pointe vers un identificateur d’entrée valide, la source de conseil est l’objet identifié par cet identificateur d’entrée. Lorsque  _lpEntryID_ est NULL, la source de conseil est la magasin de messages. 
  
Pour envoyer une notification, le fournisseur de magasin de messages ou MAPI appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de notification inscrit. L’un des paramètres **de OnNotify**, une structure de notification, contient des informations qui décrivent l’événement spécifique.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez prendre en charge les notifications avec ou sans l’aide de MAPI. MAPI dispose de trois méthodes objet de support pour aider les fournisseurs de services à implémenter la notification : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) et [IMAPISupport::Notify](imapisupport-notify.md). Si vous utilisez les méthodes de support MAPI, appelez **Subscribe** lorsque votre méthode **Advise** est appelée et relâchez le pointeur  _lpAdviseSink_ . 
  
Si vous avez choisi de prendre en charge la notification vous-même, appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du sink de notification représenté par le paramètre  _lpAdviseSink_ pour conserver une copie de ce pointeur. Conservez cette copie jusqu’à ce que [votre méthode IMsgStore::Unadvise](imsgstore-unadvise.md) soit appelée pour annuler l’inscription. 
  
Quelle que soit la prise en charge de la notification, affectez un numéro de connexion non zéro à l’inscription de la notification et renvoyez-le dans _le paramètre lpulConnection_ . Ne relâchez pas ce numéro de connexion tant **qu’Unadvise n’a** pas été appelé et n’est pas terminé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Sur les systèmes qui prendre en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut également se produire sur n’importe quel thread à tout moment. Si vous devez être certain que les notifications se produisent uniquement à un moment particulier sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet de réception de notification que vous passez à **Advise**. 
  
Une fois qu’un appel à **Advise** a réussi et avant **qu’Unadvise** ait été appelé pour annuler l’inscription, soyez prêt à libérer l’objet du reçu de conseil. Vous devez libérer votre objet de sink de conseil après le retour **de Advise** , sauf si vous avez une utilisation spécifique à long terme pour lui. 
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur la gestion des notifications, voir [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI utilise la **méthode IMsgStore::Advise** pour s’inscrire aux notifications sur l’ensemble de la boutique de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notification](notification.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

