---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326368"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Envoie une notification d'un événement spécifié à une source de notification qui a été initialement inscrite pour la notification par le biais de la méthode [IMAPISupport:: subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

_lpKey_
  
> dans Pointeur vers la clé de notification pour l'objet de source Advise. Le paramètre _lpKey_ ne peut pas être null. 
    
_cNotification_
  
> dans Nombre de structures de notification pointées par le paramètre _lpNotifications_ . 
    
_lpNotifications_
  
> dans Pointeur vers un tableau de structures de [notification](notification.md) qui décrivent des notifications en attente. 
    
_lpulFlags_
  
> [in, out] Masque de des indicateurs qui contrôle le processus de notification. Lors de l'entrée, l'indicateur suivant peut être défini:
    
  - MAPI_UNICODE 
    
    > Les chaînes dans les structures de notification pointées par _lpNotifications_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 

    Lors de la sortie, MAPI peut définir l'indicateur suivant:
        
  - NOTIFY_CANCELED 
    
    > Une fonction de rappel a annulé une notification synchrone.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les notifications ont été correctement générées.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: Notify** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services appellent **Notify** pour demander à ce qu'MAPI génère une notification pour un récepteur de notifications qui a déjà été inscrit pour la notification via la méthode **IMAPISupport:: subscribe** . 
  
**Notify** copie les structures pointées par le paramètre _lpNotifications_ en mémoire et appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur approprié. Lorsque **OnNotify** est terminé avec la notification, il libère la mémoire concernée. L'appelant n'a pas besoin d'allouer de la mémoire; MAPI effectue toute l'allocation de mémoire nécessaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La clé de notification passée dans le paramètre _lpKey_ doit être identique à la clé passée dans _lpKey_ à la méthode **IMAPISupport:: subscribe** . De nombreux fournisseurs utilisent l'identificateur d'entrée de la source de notification comme clé, mais d'autres données, telles qu'un chemin d'accès de fichier, peuvent être utilisées. MAPI utilise cette clé pour rechercher toutes les inscriptions des notifications sur la source de notification identifiée. 
  
Veillez à définir le membre **lpEntryID** de la structure de notification sur un identificateur d'entrée à long terme. 
  
Si vous définissez l'indicateur NOTIFY_SYNC sur l'appel **subscribe** pour l'une des notifications en attente, **Notify** appelle les fonctions de rappel de méthode **IMAPIAdviseSink:: OnNotify** avant de renvoyer. Un récepteur de notifications peut être créé manuellement ou en appelant [HrAllocAdviseSink](hrallocadvisesink.md). La fonction **HrAllocAdviseSink** permet à son appelant de spécifier une fonction de rappel qui **avertit** les appels dans le cadre de la notification. La fonction de rappel est conforme au prototype [NOTIFCALLBACK](notifcallback.md) . Les fonctions de rappel implémentées par les clients renvoient toujours S_OK; les fonctions de rappel implémentées par les fournisseurs de services peuvent renvoyer CALLBACK_DISCONTINUE. 
  
Si une fonction de rappel renvoie CALLBACK_DISCONTINUE, MAPI cesse d'envoyer des notifications et renvoie NOTIFY_CANCELED dans le paramètre _lpulFlags_ de la méthode **Notify** . Vous pouvez supposer que le processus est inactif et arrêter la génération de notifications pour ce processus. Si **Notify** renvoie 0 dans _lpulFlags_, le processus est toujours actif et vous devez continuer à envoyer des notifications, selon le cas.
  
Lorsque vous utilisez des notifications synchrones, veillez à éviter les situations de blocage.
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Notification](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propriété canonique PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport : IUnknown](imapisupportiunknown.md)

