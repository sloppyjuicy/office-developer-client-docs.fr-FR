---
title: IMAPISessionAdvise
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPISessionAdvise, qui s’inscrit pour recevoir la notification des événements qui affectent la session.
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
ms.openlocfilehash: 1daa131b2f7ce6ef446eff39d4af95f695e49cf9
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816590"
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du carnet d’adresses ou de l’objet de magasin de messages sur lequel les notifications doivent être générées, ou NULL, qui indique que le client s’inscrit pour recevoir des notifications sur les événements qui affectent uniquement la session. 
    
 _ulEventMask_
  
> [in] Masque de valeurs qui indiquent les types d’événements de notification qui intéressent le client et qui doivent être inclus dans l’inscription. Si  _lpEntryID a la_ valeur NULL, MAPI inscrit automatiquement le client pour les événements d’erreur critique qui affectent uniquement la session. Lorsque  _lpEntryID_ pointe vers un identificateur d’entrée, les valeurs suivantes sont valides pour le paramètre  _ulEventMask_ : 
    
fnevCriticalError 
  
> S’inscrit pour recevoir des notifications sur les erreurs graves, telles que la mémoire insuffisante.
    
fnevExtended 
  
> S’inscrit aux notifications relatives aux événements spécifiques à un carnet d’adresses ou à un fournisseur de magasin de messages particulier et à propos de l’arrêt de session.
    
fnevNewMail 
  
> S’inscrit pour les notifications concernant l’arrivée de nouveaux messages. 
    
fnevObjectCreated 
  
> S’inscrit pour les notifications relatives à la création d’un nouvel objet.
    
fnevObjectCopied
  
> S’inscrit pour les notifications concernant un objet en cours de copie.
    
fnevObjectDeleted
  
> S’inscrit pour les notifications concernant un objet en cours de suppression.
    
fnevObjectModified
  
> S’inscrit pour les notifications concernant un objet en cours de modification.
    
fnevObjectMoved
  
> S’inscrit pour les notifications concernant un objet en cours de déplacement.
    
fnevSearchComplete
  
> S’inscrit aux notifications relatives à l’achèvement d’une opération de recherche.
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet récepteur de conseil pour recevoir les notifications suivantes. Cet objet récepteur de conseil doit avoir déjà été alloué.
    
 _lpulConnection_
  
> [out] Pointeur vers un nombre différent de zéro qui représente la connexion entre l’objet récepteur conseiller de l’appelant et la session.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a réussi.
    
MAPI_E_INVALID_ENTRYID 
  
> L’identificateur d’entrée pointé par  _lpEntryID_ ne représente pas un identificateur d’entrée valide. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de services responsable de l’identificateur d’entrée pointé par  _lpEntryID_ ne prend pas en charge le type d’événements spécifié dans le paramètre _ulEventMask_ ou ne prend pas en charge la notification. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée pointé par  _lpEntryID_ ne peut être géré par aucun des fournisseurs de services dans le profil. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::Advise** établit une connexion entre l’objet récepteur conseiller de l’appelant, la session et, éventuellement, un fournisseur de services. Cette connexion est utilisée pour envoyer des notifications au récepteur de conseils quand un ou plusieurs événements spécifiés dans le paramètre _ulEventMask_ se produisent à l’objet pointé par  _lpEntryID_. Lorsque  _lpEntryID_ a la valeur NULL, l’objet cible est la session et les notifications sont envoyées uniquement pour les erreurs critiques et les événements étendus. 
  
Lorsque  _lpEntryID_ pointe vers un identificateur d’entrée valide, MAPI appelle la méthode **Advise** de l’objet d’ouverture de session qui appartient au fournisseur de services responsable. Par exemple, si  _lpEntryID_ pointe vers l’identificateur d’entrée d’une liste de distribution, MAPI appelle la méthode [IABLogon::Advise](iablogon-advise.md) du fournisseur de carnet d’adresses approprié. 
  
Pour envoyer une notification, le fournisseur de services ou MAPI appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur de conseils inscrit. L’un des paramètres **d’OnNotify**, une structure de notification, contient des informations qui décrivent l’événement spécifique.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut également se produire sur n’importe quel thread à tout moment. Si vous avez besoin de l’assurance que les notifications se produisent uniquement à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet récepteur de conseils que vous passez à la méthode **Advise** . 
  
Pour déterminer quand un client s’est déconnecté, inscrivez-vous aux notifications dans votre fournisseur de services en appelant **Conseiller** avec  _lpEntryID_ défini sur NULL et  _cbEntryID_ défini sur 0. Lorsque la fermeture de session se produit, vous recevez une notification fnevExtended. 
  
Une fois qu’un appel à **Conseiller** a réussi et [qu’IMAPISession::Unadvise](imapisession-unadvise.md) a été appelé pour annuler l’inscription, relâchez votre objet récepteur de conseils, sauf si vous avez une utilisation à long terme spécifique pour celui-ci. 
  
Pour obtenir une vue d’ensemble du processus de notification, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur la gestion des notifications, consultez [Gestion des notifications](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |MFCMAPI utilise la méthode **IMAPISession::Advise** pour s’inscrire aux notifications sur la session. |
   
## <a name="see-also"></a>Voir aussi



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Notification d’événement dans MAPI](event-notification-in-mapi.md)

