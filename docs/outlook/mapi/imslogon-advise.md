---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317310"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit un objet auprès d'un fournisseur de banque de messages pour les notifications concernant les modifications apportées à la Banque de messages. La Banque de messages enverra ensuite des notifications sur les modifications apportées à l'objet inscrit.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée de l'objet sur lequel les notifications doivent être générées. Cet objet peut être un dossier, un message ou tout autre objet dans la Banque de messages. Par ailleurs, si MAPI définit le paramètre _cbEntryID_ sur 0 et passe la **valeur null** pour _lpEntryID_, le récepteur de notifications fournit des notifications sur les modifications apportées à la Banque de messages entière.
    
 _ulEventMask_
  
> dans Un masque d'événement des types d'événements de notification survenus pour l'objet sur lequel MAPI générera des notifications. Le masque filtre des cas spécifiques. Chaque type d'événement est associé à une structure qui contient des informations supplémentaires sur l'événement. Le tableau suivant répertorie les types d'événement possibles ainsi que les structures correspondantes.
    
|**Type d'événement de notification**|**Structure correspondante**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> dans Pointeur vers un objet de récepteur de notification à appeler lorsqu'un événement de l'objet session a été demandé. Cet objet de récepteur de notifications doit déjà exister.
    
 _lpulConnection_
  
> remarquer Un pointeur vers une variable qui, lorsqu'un retour réussi, conserve le numéro de connexion pour l'enregistrement de la notification. Le numéro de connexion doit être différent de zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L'opération n'est pas prise en charge par MAPI ou par un ou plusieurs fournisseurs de services.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de banque de messages implémentent la méthode **IMSLogon:: Advise** pour enregistrer un objet pour les rappels de notification. Chaque fois qu'une modification est apportée à l'objet indiqué, le fournisseur vérifie le bit de masque d'événement qui a été défini dans le paramètre _ulEventMask_ et, par conséquent, le type de modification qui a eu lieu. Si un bit est défini, le fournisseur appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet de récepteur de notifications indiqué par le paramètre _lpAdviseSink_ pour signaler l'événement. Les données transmises dans la structure de notification à la routine **OnNotify** décrivent l'événement. 
  
L'appel à **OnNotify** peut se produire pendant l'appel qui modifie l'objet ou ultérieurement. Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut se produire sur n'importe quel thread. Pour gérer en toute sécurité un appel à **OnNotify** susceptible de se produire à un moment inopportun, une application cliente doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Pour fournir des notifications, le fournisseur de banque de messages qui implémente l' **avis** doit conserver une copie du pointeur vers l'objet récepteur _lpAdviseSink_ . pour ce faire, le fournisseur appelle la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour le récepteur de notifications afin de maintenir son pointeur d'objet jusqu'à ce que l'enregistrement de notification soit annulé avec un appel à la méthode [IMSLogon::](imslogon-unadvise.md) Unadvise. L'implémentation de l' **avis** doit affecter un numéro de connexion à l'enregistrement des notifications et appeler **AddRef** sur ce numéro de connexion avant de le renvoyer dans le paramètre _lpulConnection_ . Les fournisseurs de services peuvent libérer l'objet récepteur de notification avant l'annulation de l'inscription, mais ils ne doivent pas libérer **** le numéro de connexion tant qu'Unadvise n'a pas été appelé. 
  
Une fois qu'un **** appel à Advise a réussi et avant que Unadvise ait été appelé, les fournisseurs doivent être préparés pour que l'objet de récepteur de notifications soit publié. **** Par conséquent, un fournisseur doit libérer son objet de récepteur **** de notification une fois qu'il a été renvoyé, sauf s'il a une utilisation longue durée spécifique pour lui. 
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Notification](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

