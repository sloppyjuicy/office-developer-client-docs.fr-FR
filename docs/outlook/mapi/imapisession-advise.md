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
ms.openlocfilehash: 704a556b97f5fd90989641a17afe5a11d127e51b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577169"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la session.
  
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
  
> [in] Pointeur vers l’identificateur d’entrée du carnet d’adresses objet de banque de messages sur les notifications doivent être générées ou valeur NULL, ce qui indique que le client s’inscrit pour recevoir des notifications concernant les événements qui affectent uniquement la session. 
    
 _ulEventMask_
  
> [in] Un masque des valeurs qui indiquent les types d’événements de notification que le client s’intéresse et doit être inclus dans l’enregistrement. Si _lpEntryID_ est NULL, MAPI enregistre automatiquement le client pour les événements d’erreur critique qui affectent uniquement la session. Lorsque _lpEntryID_ pointe vers un identificateur d’entrée, les valeurs suivantes sont valides pour le paramètre _ulEventMask_ : 
    
fnevCriticalError 
  
> Enregistre les notifications sur les erreurs graves, telles que la mémoire insuffisante.
    
fnevExtended 
  
> Registres notifications concernant les événements spécifiques à un carnet d’adresses ou un message de fournisseur de magasins et sur la session arrêté.
    
fnevNewMail 
  
> Enregistre les notifications relatives à l’arrivée de nouveaux messages. 
    
fnevObjectCreated 
  
> Enregistre les notifications concernant la création d’un nouvel objet.
    
fnevObjectCopied
  
> Enregistre les notifications relatives à un objet en cours de copie.
    
fnevObjectDeleted
  
> Enregistre les notifications relatives à un objet en cours de suppression.
    
fnevObjectModified
  
> Enregistre les notifications relatives à un objet en cours de modification.
    
fnevObjectMoved
  
> Enregistre les notifications relatives à un objet en cours de déplacement.
    
fnevSearchComplete
  
> Enregistre les notifications relatives à la fin d’une opération de recherche.
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures. Cet objet de récepteur advise doit déjà affectée.
    
 _lpulConnection_
  
> [out] Un pointeur vers un nombre différent de zéro qui représente la connexion entre l’appelant de notification objet récepteur et la session.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L’identificateur d’entrée désigné par _lpEntryID_ ne représente pas un identificateur d’entrée valide. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de services responsable de l’identificateur d’entrée désigné par _lpEntryID_ ne prend pas en charge le type d’événements spécifié dans le paramètre _ulEventMask_ ou ne prend pas en charge la notification. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée désigné par _lpEntryID_ ne peut pas être géré par les fournisseurs de services dans le profil. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::Advise** établit une connexion entre l’appelant d’informer l’objet récepteur, la session et, éventuellement, un fournisseur de services. Cette connexion est utilisée pour envoyer des notifications pour le récepteur de notifications lorsqu’un ou plusieurs événements spécifiés dans le paramètre _ulEventMask_ se produisent sur l’objet vers lequel pointé _lpEntryID_. Lorsque _lpEntryID_ est NULL, l’objet cible est la session et les notifications sont envoyées uniquement pour les erreurs critiques et les événements étendus. 
  
Lorsque _lpEntryID_ pointe vers un identificateur d’entrée valide, la méthode **Advise** de l’objet d’ouverture de session qui appartient au fournisseur de services responsable appels MAPI. Par exemple, si _lpEntryID_ pointe vers l’identificateur d’entrée d’une liste de distribution, MAPI appelle la méthode de [IABLogon::Advise](iablogon-advise.md) du fournisseur livre adresse appropriée. 
  
Pour envoyer une notification, le fournisseur de services ou MAPI appelle méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur des notifications. L’un des paramètres à **OnNotify**, une structure de notification, contient des informations décrivant l’événement spécifique.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut également se produire sur n’importe quel thread à tout moment. Si vous avez besoin pour l’assurance que des notifications seront produit uniquement à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet récepteur advise que vous passez à la méthode **Advise** . 
  
Pour déterminer si un client est déconnecté, inscrire pour les notifications dans votre fournisseur de services en appelant **Advise** _lpEntryID_ défini sur NULL et _cbEntryID_ définie sur 0. Lors de la fermeture de session se produit, vous recevez une notification fnevExtended. 
  
Après qu’un appel à **Advise** a réussi et avant [IMAPISession::Unadvise](imapisession-unadvise.md) a été appelé pour annuler l’inscription, mise à jour votre objet de réception de notifications à moins d’avoir une utilisation à long terme spécifique pour qu’il. 
  
Pour une vue d’ensemble du processus de notification, voir la [Notification d’événement MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur la gestion des notifications, voir [Gestion des Notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI utilise la méthode **IMAPISession::Advise** pour enregistrer les notifications par rapport à la session.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Notification d’événement MAPI](event-notification-in-mapi.md)

