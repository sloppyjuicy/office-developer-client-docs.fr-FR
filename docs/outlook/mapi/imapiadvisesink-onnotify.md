---
title: IMAPIAdviseSinkOnNotify
description: IMAPIAdviseSinkOnNotify répond à une notification en effectuant une ou plusieurs tâches, qui dépendent du type d’événement et d’objet qui génèrent la notification.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
ms.openlocfilehash: d7bdbf2e86567bfe8c064c39e3f79a8d63ecf3b2
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818179"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Répond à une notification en effectuant une ou plusieurs tâches. Les tâches effectuées dépendent du type d’événement et de l’objet qui génère la notification. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Paramètres

 _cNotif_
  
> [in] Nombre de structures [NOTIFICATION](notification.md) pointées par le paramètre  _lpNotifications_ . 
    
 _lpNotifications_
  
> [in] Pointeur vers une ou plusieurs structures **NOTIFICATION** qui fournissent des informations sur les événements qui se sont produits. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a été traitée avec succès.
    
## <a name="remarks"></a>Remarques

Le processus de notification démarre lorsqu’un client ou MAPI effectue un appel à la méthode **Conseiller** d’un fournisseur de services pour s’inscrire afin de recevoir une notification d’un type particulier pour un objet particulier. L’un des paramètres de la méthode **Advise** est un pointeur vers un objet récepteur de conseils qui implémente l’interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Lorsqu’un événement se produit sur l’objet cible qui correspond à la notification inscrite, le fournisseur de services, directement ou indirectement via MAPI, appelle la méthode **OnNotify** du récepteur de conseils. 
  
L’appel à **OnNotify** peut se produire pendant l’appel MAPI à l’origine de l’événement ou ultérieurement. Sur les systèmes qui prennent en charge plusieurs threads d’exécution, **OnNotify** peut être appelé sur le même thread que celui utilisé pour l’inscription ou sur un autre thread. Les clients peuvent s’assurer que l’appel **OnNotify** est effectué sur le même thread que celui utilisé pour appeler **Conseiller** en créant le récepteur de conseils qu’ils passent à **Conseiller** avec la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Le paramètre  _lpNotifications_ pointe vers une ou plusieurs structures **NOTIFICATION** qui décrivent ce qui a changé pendant l’événement. Il existe un type **différent de structure** NOTIFICATION pour chaque type d’événement. 
  
Le tableau suivant répertorie les valeurs utilisées pour représenter les types d’événements possibles et les structures associées à chaque valeur :
  
|**Type d’événement de notification**|**Structure correspondante**|
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
   
Pour plus d’informations sur la configuration et l’arrêt des notifications, consultez les entrées de référence pour les méthodes **Advise** et **Unadvise** pour l’une des interfaces suivantes : [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md) et [IMSLogon](imslogoniunknown.md). 
  
Pour obtenir des informations générales sur le processus de notification, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Votre implémentation **OnNotify** se compose généralement d’un ou de plusieurs blocs de code pour chaque type de notification que vous prévoyez de recevoir. Dans ces blocs de code, effectuez toutes les tâches que vous jugez nécessaires en réponse à la notification. Par exemple, supposons que vous vous inscrivez pour recevoir des notifications **fnevObjectModified** sur un dossier inclus dans un affichage de boîte de dialogue. Dans le bloc de code que vous incluez dans votre méthode **OnNotify** pour gérer les notifications **fnevObjectModified**, vous pouvez envoyer un message Windows à la boîte de dialogue pour demander un affichage mis à jour. 
  
Ne modifiez pas ou ne libérez pas la structure **NOTIFICATION** passée à **OnNotify**. Les données de la structure sont valides uniquement jusqu’à ce **qu’OnNotify** retourne. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque des modifications sont apportées à plusieurs objets, vous pouvez notifier un récepteur de conseils inscrit dans un seul appel à **OnNotify** ou dans plusieurs appels en fonction des contraintes de mémoire. Cela est vrai, que les modifications soient le résultat d’un appel de méthode ou de plusieurs. Par exemple, un appel à [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) peut affecter plusieurs messages et dossiers. En tant que fournisseur de magasin de messages, vous pouvez effectuer un appel à **OnNotify** avec un type **d’événement fnevObjectModified** pour le dossier cible ou de nombreux appels, un pour chaque message affectant. De même, si un client effectue des appels [répétés à IMAPIFolder::CreateMessage](imapifolder-createmessage.md), ces appels peuvent être combinés en un événement **fnevObjectModified** pour le dossier ou séparés en événements **fnevObjectCreated** individuels pour chaque nouveau message. 
  
Pour plus d’informations sur la façon et le moment de générer des notifications, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md) et [Notification d’événement de prise en charge](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AdviseSink.h et AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |La classe CAdviseSink est implémentée pour gérer toutes les notifications dans MFCMAPI. |
   
## <a name="see-also"></a>Voir aussi



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notification](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

