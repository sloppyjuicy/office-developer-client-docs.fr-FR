---
title: IMsgStoreAdvise
description: IMsgStore Conseille aux registres de recevoir une notification des événements spécifiés qui affectent le magasin de messages.
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
ms.openlocfilehash: 79ce405feee4cdbd01d98ef383235f7fd07595a8
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828170"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
S’inscrit pour recevoir une notification des événements spécifiés qui affectent le magasin de messages.
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier ou du message sur lequel les notifications doivent être générées, ou **null**. Si  _lpEntryID_ est défini sur NULL, **conseillez** les inscriptions pour les notifications sur l’ensemble du magasin de messages. 
    
 _ulEventMask_
  
> [in] Masque de valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et doivent être inclus dans l’inscription. Une structure [NOTIFICATION](notification.md) correspondante est associée à chaque type d’événement qui contient des informations sur l’événement. Les valeurs suivantes sont valides pour le paramètre  _ulEventMask_ : 
    
 _fnevCriticalError_
  
> S’inscrit pour recevoir des notifications sur les erreurs graves, telles que la mémoire insuffisante.
    
 _fnevExtended_
  
> S’inscrit pour les notifications relatives aux événements spécifiques au fournisseur de magasin de messages particulier.
    
 _fnevNewMail_
  
> S’inscrit pour les notifications concernant l’arrivée de nouveaux messages. 
    
 _fnevObjectCreated_
  
> S’inscrit aux notifications relatives à la création d’un dossier ou d’un message.
    
 _fnevObjectCopied_
  
> S’inscrit pour les notifications concernant un dossier ou un message en cours de copie.
    
 _fnevObjectDeleted_
  
> S’inscrit pour les notifications concernant un dossier ou un message en cours de suppression.
    
 _fnevObjectModified_
  
> S’inscrit pour les notifications concernant un dossier ou un message en cours de modification.
    
 _fnevObjectMoved_
  
> S’inscrit pour les notifications concernant un dossier ou un message en cours de déplacement.
    
 _fnevSearchComplete_
  
> S’inscrit aux notifications relatives à l’achèvement d’une opération de recherche.
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet récepteur de conseil pour recevoir les notifications suivantes. Cet objet récepteur de conseil doit avoir déjà été alloué.
    
 _lpulConnection_
  
> [out] Pointeur vers un nombre différent de zéro qui représente la connexion entre l’objet récepteur conseiller de l’appelant et la session. 
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet récepteur de conseil pour recevoir les notifications suivantes. Cet objet récepteur de conseil doit avoir déjà été alloué. 
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro de connexion différent de zéro qui représente la connexion entre l’objet récepteur conseiller de l’appelant et le magasin de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a réussi.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur du magasin de messages ne prend pas en charge l’inscription pour la notification via le magasin de messages.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::Advise** établit une connexion entre l’objet récepteur conseiller de l’appelant et le magasin de messages ou un objet dans le magasin de messages. Cette connexion est utilisée pour envoyer des notifications au récepteur de conseils lorsqu’un ou plusieurs événements, comme spécifié dans le paramètre _ulEventMask_ , se produisent à l’objet source conseiller. Lorsque le paramètre  _lpEntryID_ pointe vers un identificateur d’entrée valide, la source de conseil est l’objet identifié par cet identificateur d’entrée. Lorsque  _lpEntryID_ a la valeur NULL, la source de conseil est le magasin de messages. 
  
Pour envoyer une notification, le fournisseur du magasin de messages ou MAPI appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur de conseils inscrit. L’un des paramètres **d’OnNotify**, une structure de notification, contient des informations qui décrivent l’événement spécifique.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez gérer les notifications avec ou sans l’aide de MAPI. MAPI propose trois méthodes d’objet de support pour aider les fournisseurs de services à implémenter la notification : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) et [IMAPISupport::Notify](imapisupport-notify.md). Si vous choisissez d’utiliser les méthodes de support MAPI, appelez **Subscribe** lorsque votre méthode **Advise** est appelée et relâchez le pointeur  _lpAdviseSink_ . 
  
Si vous choisissez de prendre en charge la notification vous-même, appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du récepteur conseiller représenté par le paramètre  _lpAdviseSink_ pour conserver une copie de ce pointeur. Conservez cette copie jusqu’à ce que votre méthode [IMsgStore::Unadvise](imsgstore-unadvise.md) soit appelée pour annuler l’inscription. 
  
Quelle que soit la façon dont vous prenez en charge la notification, attribuez un numéro de connexion différent de zéro à l’inscription de notification et retournez-le dans le paramètre _lpulConnection_ . Ne relâchez pas ce numéro de connexion tant **qu’Unadvise** n’a pas été appelé et n’est pas terminé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut également se produire sur n’importe quel thread à tout moment. Si vous devez être certain que les notifications se produisent uniquement à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet récepteur de conseils que vous passez à **Conseiller**. 
  
Une fois qu’un appel à **Conseiller** a réussi et **qu’Unadvise** a été appelé pour annuler l’inscription, préparez-vous à la libération de l’objet récepteur de conseil. Vous devez libérer votre objet récepteur de conseils après le retour de **Conseiller** , sauf si vous avez une utilisation à long terme spécifique pour celui-ci. 
  
Pour plus d’informations sur le processus de notification, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur la gestion des notifications, consultez [Gestion des notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI utilise la méthode **IMsgStore::Advise** pour s’inscrire aux notifications sur l’ensemble du magasin de messages. |
   
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[Notification](notification.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

