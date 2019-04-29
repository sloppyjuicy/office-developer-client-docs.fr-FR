---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407360"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Répond à une notification en effectuant une ou plusieurs tâches. Les tâches effectuées dépendent du type d'événement et de l'objet qui génère la notification. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Paramètres

 _cNotif_
  
> dans Nombre de structures de [notification](notification.md) pointées par le paramètre _lpNotifications_ . 
    
 _lpNotifications_
  
> dans Pointeur vers une ou plusieurs structures de **notification** qui fournissent des informations sur les événements qui se sont produits. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a été correctement traitée.
    
## <a name="remarks"></a>Remarques

Le processus de notification démarre lorsqu'un client ou MAPI effectue un appel à la méthode **Advise** d'un fournisseur de services pour s'inscrire afin de recevoir une notification d'un type particulier pour un objet particulier. L'un des paramètres de la **** méthode Advise est un pointeur vers un objet de récepteur de notification qui implémente l'interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Lorsqu'un événement se produit dans l'objet cible qui correspond à la notification enregistrée, le fournisseur de services, directement ou indirectement via MAPI, appelle la méthode **OnNotify** du récepteur de notification. 
  
L'appel à **OnNotify** peut se produire soit lors de l'appel MAPI qui provoque l'événement, soit ultérieurement. Sur les systèmes qui prennent en charge plusieurs threads d'exécution, **OnNotify** peut être appelé sur le même thread qui a été utilisé pour l'inscription ou sur un autre thread. Les clients peuvent s'assurer que l'appel **OnNotify** est effectué sur le même thread que celui utilisé pour appeler Advise en créant le récepteur de **** notifications qu'ils passent à la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . **** 
  
Le paramètre _lpNotifications_ pointe vers une ou plusieurs structures de **notification** qui décrivent les modifications apportées au cours de l'événement. Il existe un autre type de structure de **notification** pour chaque type d'événement. 
  
Le tableau suivant répertorie les valeurs qui sont utilisées pour représenter les types possibles d'événements et les structures associées à chaque valeur:
  
|**Type d'événement de notification**|**Structure correspondante**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevNewMail** <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevSearchComplete** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
|**fnevStatusObjectModified** <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
|**fnevExtended** <br/> |[EXTENDED_NOTIFICATION](extended_notification.md) <br/> |
   
Pour plus d'informations sur la configuration et l'arrêt des notifications, consultez les entrées de **** référence pour les méthodes Advise et Unadvise pour l'une des interfaces suivantes: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), **** [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)et [IMSLogon](imslogoniunknown.md). 
  
Pour obtenir des informations générales sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Votre implémentation de **OnNotify** se compose généralement d'un ou de plusieurs blocs de code pour chaque type de notification que vous prévoyez de recevoir. À l'intérieur de ces blocs de code, effectuez toutes les tâches que vous jugez nécessaires en réponse à la notification. Par exemple, supposons que vous vous inscrivez pour recevoir des notifications **fnevObjectModified** sur un dossier qui est inclus dans un affichage de boîte de dialogue. Dans le bloc de code que vous incluez dans votre méthode **OnNotify** pour gérer les notifications **fnevObjectModified** , vous pouvez envoyer un message Windows à la boîte de dialogue pour demander un affichage mis à jour. 
  
Ne modifiez pas ou ne libérez pas la structure de **notification** transmise à **OnNotify**. Les données de la structure sont valides uniquement jusqu'à ce que **OnNotify** renvoie. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque des modifications sont apportées à plusieurs objets, vous pouvez avertir un récepteur de notifications enregistré en un seul appel à **OnNotify** ou dans plusieurs appels en fonction des contraintes de mémoire. Cela est vrai, que les modifications soient le résultat d'un ou de plusieurs appels de méthode. Par exemple, un appel à [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) peut affecter plusieurs messages et dossiers. En tant que fournisseur de banque de messages, vous pouvez passer un appel à **OnNotify** avec un type d'événement **fnevObjectModified** pour le dossier cible ou de nombreux appels, un pour chacun affecte les messages. De même, si un client effectue des appels répétés à [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md), ces appels peuvent être combinés en un seul événement **fnevObjectModified** pour le dossier ou être séparés en événements **fnevObjectCreated** individuels pour chaque nouveau message. 
  
Pour plus d'informations sur la génération de notifications, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md) et [notification d'événement de prise en charge](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AdviseSink. h et AdviseSink. cpp  <br/> |CAdviseSink:: OnNotifyDesc  <br/> |La classe CAdviseSink est implémentée pour gérer toutes les notifications dans MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notification](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

