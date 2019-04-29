---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419834"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
S'inscrit pour recevoir des notifications d'événements spécifiques affectant la session.
  
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
  
> dans Pointeur vers l'identificateur d'entrée du carnet d'adresses ou de l'objet de banque de messages sur les notifications à générer, ou valeur NULL, qui indique que le client s'inscrit pour recevoir des notifications sur les événements qui affectent uniquement la session. 
    
 _ulEventMask_
  
> dans Masque de valeurs qui indiquent les types d'événements de notification qui intéressent le client et qui doivent être inclus dans l'inscription. Si _lpEntryID_ est null, MAPI inscrit automatiquement le client pour les événements d'erreur critique qui affectent uniquement la session. Lorsque _lpEntryID_ pointe vers un identificateur d'entrée, les valeurs suivantes sont valides pour le paramètre _ulEventMask_ : 
    
fnevCriticalError 
  
> Enregistre les notifications concernant les erreurs graves, telles que la mémoire insuffisante.
    
fnevExtended 
  
> S'inscrit pour les notifications concernant des événements spécifiques à un carnet d'adresses ou un fournisseur de banque de messages particulier et sur la fermeture de session.
    
fnevNewMail 
  
> Enregistre les notifications relatives à l'arrivée de nouveaux messages. 
    
fnevObjectCreated 
  
> Enregistre les notifications relatives à la création d'un nouvel objet.
    
fnevObjectCopied
  
> Enregistre les notifications relatives à un objet en cours de copie.
    
fnevObjectDeleted
  
> Enregistre les notifications relatives à la suppression d'un objet.
    
fnevObjectModified
  
> Enregistre les notifications relatives à un objet modifié.
    
fnevObjectMoved
  
> Enregistre les notifications relatives à un objet déplacé.
    
fnevSearchComplete
  
> Enregistre les notifications relatives à l'exécution d'une opération de recherche.
    
 _lpAdviseSink_
  
> dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes. Cet objet de récepteur de notifications doit déjà avoir été alloué.
    
 _lpulConnection_
  
> remarquer Pointeur vers un nombre différent de zéro qui représente la connexion entre l'objet de récepteur d'avertissement de l'appelant et la session.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'inscription a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L'identificateur d'entrée pointé par _lpEntryID_ ne représente pas un identificateur d'entrée valide. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de services responsable de l'identificateur d'entrée désigné par _lpEntryID_ ne prend pas en charge le type d'événements spécifiés dans le paramètre _ulEventMask_ ou ne prend pas en charge la notification. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L'identificateur d'entrée pointé par _lpEntryID_ ne peut pas être géré par les fournisseurs de services dans le profil. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: Advise** établit une connexion entre l'objet récepteur de notification de l'appelant, la session et, éventuellement, un fournisseur de services. Cette connexion est utilisée pour envoyer des notifications au récepteur de notifications lorsqu'un ou plusieurs événements spécifiés dans le paramètre _ulEventMask_ se produisent dans l'objet désigné par _lpEntryID_. Lorsque _lpEntryID_ est null, l'objet cible est la session et les notifications sont envoyées uniquement pour les erreurs critiques et les événements étendus. 
  
Lorsque _lpEntryID_ pointe vers un identificateur d'entrée valide, MAPI appelle la **** méthode Advise de l'objet Logon qui appartient au fournisseur de services responsable. Par exemple, si _lpEntryID_ pointe sur l'identificateur d'entrée d'une liste de distribution, MAPI appelle la méthode [IABLogon:: Advise](iablogon-advise.md) du fournisseur de carnet d'adresses approprié. 
  
Pour envoyer une notification, le fournisseur de services ou MAPI appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de notification enregistré. L'un des paramètres de **OnNotify**, une structure de notification, contient des informations qui décrivent l'événement spécifique.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut également se produire sur n'importe quel thread à tout moment. Si vous avez besoin d'assurance que les notifications ne se produiront qu'à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l'objet de récepteur de notifications que vous transmettez à la méthode Advise. **** 
  
Pour déterminer quand un client a fermé une session, inscrivez-vous aux notifications dans votre **** fournisseur de services en appelant Advise avec _LPENTRYID_ défini sur null et _cbEntryID_ défini sur 0. Lorsque la déconnexion se produit, vous recevez une notification fnevExtended. 
  
Une fois qu'un **** appel à Advise a réussi et avant [IMAPISession::](imapisession-unadvise.md) Unadvise a été appelé pour annuler l'inscription, libérer votre objet de récepteur de Conseil, sauf si vous disposez d'une utilisation de longue durée spécifique. 
  
Pour obtenir une vue d'ensemble du processus de notification, consultez la rubrique notifications d' [événements dans MAPI](event-notification-in-mapi.md). 
  
Pour plus d'informations sur la gestion des notifications, consultez la rubrique [gestion](handling-notifications.md)des notifications. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnNotificationsOn  <br/> |MFCMAPI utilise la méthode **IMAPISession:: Advise** pour s'inscrire aux notifications par rapport à la session.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Notification d'événement dans MAPI](event-notification-in-mapi.md)

