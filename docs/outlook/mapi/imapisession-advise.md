---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f7fcfb54b3ca0a07a6dfc30099189da2f7aac2be
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784047"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
S’inscrit pour recevoir une notification des événements spécifiés qui affectent la session.
  
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
  
> [in] Pointeur vers l’identificateur d’entrée du carnet d’adresses ou de l’objet de magasin de messages sur les notifications à générer, ou NULL, qui indique que le client s’inscrit pour recevoir des notifications sur les événements qui affectent uniquement la session. 
    
 _ulEventMask_
  
> [in] Masque de valeurs qui indiquent les types d’événements de notification qui intéressent le client et qui doivent être inclus dans l’inscription. Si  _lpEntryID_ est NULL, MAPI inscrit automatiquement le client pour les événements d’erreur critiques qui affectent uniquement la session. Lorsque  _lpEntryID_ pointe vers un identificateur d’entrée, les valeurs suivantes sont valides pour le  _paramètre ulEventMask_ : 
    
fnevCriticalError 
  
> S’inscrit aux notifications concernant les erreurs graves, telles que la mémoire insuffisante.
    
fnevExtended 
  
> S’inscrit aux notifications sur les événements spécifiques à un fournisseur de carnet d’adresses ou de magasin de messages particulier et sur l’arrêt de la session.
    
fnevNewMail 
  
> S’inscrit aux notifications concernant l’arrivée de nouveaux messages. 
    
fnevObjectCreated 
  
> S’inscrit aux notifications concernant la création d’un nouvel objet.
    
fnevObjectCopied
  
> S’inscrit aux notifications concernant un objet en cours de copie.
    
fnevObjectDeleted
  
> S’inscrit aux notifications concernant un objet en cours de suppression.
    
fnevObjectModified
  
> S’inscrit aux notifications concernant un objet modifié.
    
fnevObjectMoved
  
> S’inscrit aux notifications concernant un objet déplacé.
    
fnevSearchComplete
  
> S’inscrit aux notifications concernant la fin d’une opération de recherche.
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes. Cet objet de sink de conseil doit avoir déjà été alloué.
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro autre que zéro qui représente la connexion entre l’objet de l’objet de conseiller de l’appelant et la session.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L’identificateur d’entrée pointé  _par lpEntryID_ ne représente pas un identificateur d’entrée valide. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de services responsable de l’identificateur d’entrée pointé par  _lpEntryID_ ne prend pas en charge le type d’événements spécifié dans le paramètre _ulEventMask_ ou ne prend pas en charge la notification. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée pointé par  _lpEntryID_ ne peut être géré par aucun des fournisseurs de services dans le profil. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::Advise** établit une connexion entre l’objet de l’objet de conseiller de l’appelant, la session et éventuellement un fournisseur de services. Cette connexion est utilisée pour envoyer des notifications au réception de notification lorsqu’un ou plusieurs événements spécifiés dans le paramètre _ulEventMask_ se produisent à l’objet pointé par  _lpEntryID_. Lorsque  _lpEntryID_ est NULL, l’objet cible est la session et les notifications sont envoyées uniquement pour les erreurs critiques et les événements étendus. 
  
Lorsque  _lpEntryID_ pointe vers un identificateur d’entrée valide, MAPI appelle la méthode **Advise** de l’objet d’inscription qui appartient au fournisseur de services responsable. Par exemple, si  _lpEntryID_ pointe vers l’identificateur d’entrée d’une liste de distribution, MAPI appelle la méthode [IABLogon::Advise](iablogon-advise.md) du fournisseur de carnet d’adresses approprié. 
  
Pour envoyer une notification, le fournisseur de services ou MAPI appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de notification inscrit. L’un des paramètres **de OnNotify**, une structure de notification, contient des informations qui décrivent l’événement spécifique.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Sur les systèmes qui prendre en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut également se produire sur n’importe quel thread à tout moment. Si vous avez besoin d’assurance que les notifications ne se produisent qu’à un moment particulier sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet de réception de notification que vous passez à la méthode **Advise** . 
  
Pour déterminer quand un client s’est déconnecté, inscrivez-vous aux notifications dans votre fournisseur de services en appelant **Advise** avec  _lpEntryID_ sur NULL et  _cbEntryID_ sur 0. Lorsque la logoff se produit, vous recevez une notification fnevExtended. 
  
Une fois qu’un appel à **Advise** a réussi et avant que [IMAPISession::Unadvise](imapisession-unadvise.md) ait été appelé pour annuler l’inscription, relâchez votre objet de sink de conseil, sauf si vous avez une utilisation spécifique à long terme pour celui-ci. 
  
Pour une vue d’ensemble du processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur la gestion des notifications, voir [Handling Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI utilise la **méthode IMAPISession::Advise** pour s’inscrire aux notifications par rapport à la session. |
   
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Notification d’événement dans MAPI](event-notification-in-mapi.md)

