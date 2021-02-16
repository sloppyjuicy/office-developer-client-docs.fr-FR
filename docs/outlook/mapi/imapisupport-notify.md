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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435935"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Envoie une notification d’un événement spécifié à une source de conseil qui s’est inscrite à l’origine pour la notification via la méthode [IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
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
  
> [in] Pointeur vers la clé de notification pour l’objet source de notification. Le  _paramètre lpKey_ ne peut pas être NULL. 
    
_cNotification_
  
> [in] Nombre de structures de notifications pointées par _le paramètre lpNotifications._ 
    
_lpNotifications_
  
> [in] Pointeur vers un tableau de structures [de NOTIFICATION](notification.md) qui décrivent les notifications en attente. 
    
_lpulFlags_
  
> [in, out] Masque de bits d’indicateurs qui contrôle le processus de notification. Lors de l’entrée, l’indicateur suivant peut être définie :
    
  - MAPI_UNICODE 
    
    > Les chaînes dans les structures de notification pointées par  _lpNotifications_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 

    Lors de la sortie, MAPI peut définir l’indicateur suivant :
        
  - NOTIFY_CANCELED 
    
    > Une fonction de rappel a annulé une notification synchrone.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les notifications ont été correctement générées.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::Notify** est implémentée pour tous les objets de support du fournisseur de services. Les fournisseurs de services appellent **Notify** pour demander à MAPI de générer une notification pour un recevoir de notification qui s’est précédemment inscrit pour la notification via la méthode **IMAPISupport::Subscribe.** 
  
**Notify** copie les structures pointées vers le paramètre  _lpNotifications_ dans la mémoire et appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de notification approprié. Une fois la notification terminée, **OnNotify** libère la mémoire impliquée. L’appelant n’a pas besoin d’allouer de mémoire . MAPI effectue toutes les allocations de mémoire nécessaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La clé de notification transmise dans le paramètre _lpKey_ doit être identique à la clé transmise dans _lpKey_ à la méthode **IMAPISupport::Subscribe.** De nombreux fournisseurs utilisent l’identificateur d’entrée de la source de conseil comme clé, mais d’autres données, telles qu’un chemin d’accès au fichier, peuvent être utilisées. MAPI utilise cette clé pour rechercher toutes les inscriptions pour les notifications sur la source de notification identifiée. 
  
Assurez-vous de définir le membre **lpEntryID** de la structure de notification sur un identificateur d’entrée à long terme. 
  
Si vous définissez l’indicateur  NOTIFY_SYNC sur l’appel d’abonnement pour l’une des notifications en attente, **Notify** appelle les fonctions de rappel de méthode **IMAPIAdviseSink::OnNotify** avant de renvoyer. Un sink de conseil peut être créé manuellement ou en appelant [HrAllocAdviseSink](hrallocadvisesink.md). La **fonction HrAllocAdviseSink** permet à son appelant de  spécifier une fonction de rappel qui notifie les appels dans le cadre de la notification. La fonction de rappel est conforme au prototype [NOTIFCALLBACK.](notifcallback.md) Les fonctions de rappel implémentées par les clients retournent toujours S_OK ; les fonctions de rappel implémentées par les fournisseurs de services peuvent renvoyer CALLBACK_DISCONTINUE. 
  
Si une fonction de rappel renvoie CALLBACK_DISCONTINUE, MAPI cesse d’envoyer des notifications et renvoie NOTIFY_CANCELED dans le paramètre _lpulFlags_ de la méthode **Notify.** Vous pouvez supposer que le processus est inactif et arrêter de générer des notifications pour ce processus. Si **Notify** renvoie 0 dans  _lpulFlags,_ le processus est toujours actif et vous devez continuer à envoyer des notifications, le cas échéant.
  
Lorsque vous utilisez des notifications synchrones, évitez les blocages.
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Notification](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propriété canonique PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport : IUnknown](imapisupportiunknown.md)

