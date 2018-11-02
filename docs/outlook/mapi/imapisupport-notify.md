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
ms.openlocfilehash: f79e5eaa3155bbe3373f5ad9c5182a4a65c62648
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572038"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Envoie une notification d’un événement spécifié à une source d’advise initialement enregistré pour la notification par le biais de la méthode [IMAPISupport::Subscribe](imapisupport-subscribe.md) . 
  
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
  
> [in] Pointeur vers la clé de notification pour l’objet source de notification. Le paramètre _lpKey_ ne peut pas être NULL. 
    
_cNotification_
  
> [in] Le nombre de structures de notification indiqué par le paramètre _lpNotifications_ . 
    
_lpNotifications_
  
> [in] Pointeur vers un tableau de structures [NOTIFICATION](notification.md) qui décrivent les notifications en attente. 
    
_lpulFlags_
  
> [entrée, sortie] Masque de bits d’indicateurs qui contrôle le processus de notification. À l’entrée, l’indicateur suivant peut être définie :
    
  - MAPI_UNICODE 
    
    > Les chaînes dans les structures de notification désignés par _lpNotifications_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 

    Dans la sortie, MAPI permettre définir l’indicateur suivant :
        
  - NOTIFY_CANCELED 
    
    > Une fonction de rappel annulé une notification synchrone.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les notifications ont été correctement générées.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::Notify** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services d’appel **notifier** pour demander que MAPI générer une notification pour un récepteur de notifications qui a précédemment inscrit pour la notification par le biais de la méthode **IMAPISupport::Subscribe** . 
  
Copies **notifier** les structures désignés par le paramètre _lpNotifications_ dans la mémoire et appelle la méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise approprié. Lors de la notification **OnNotify** est terminé, il libère la mémoire impliqués. L’appelant n’a pas besoin d’allouer de la mémoire ; MAPI effectue toutes les l’allocation de mémoire nécessaire. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La clé de notification passée dans le paramètre _lpKey_ doit être identique à la clé _lpKey_ passée à la méthode **IMAPISupport::Subscribe** . De nombreux fournisseurs utilisent l’identificateur d’entrée de la source advise comme clé, mais autres données, telles que d’un chemin d’accès du fichier, peuvent être utilisées. MAPI utilise cette clé pour rechercher tous les enregistrements pour les notifications sur la source advise identifiés. 
  
N’oubliez pas que vous définissez le membre **lpEntryID** de la structure de notification sur un identificateur d’entrée à long terme. 
  
Si vous définissez l’indicateur NOTIFY_SYNC sur l' **abonnement** appels pour les notifications en attente, **notifier** les fonctions de rappel de méthode **IMAPIAdviseSink::OnNotify** avant de retourner. Un récepteur de notifications peut être créé manuellement ou en appelant [HrAllocAdviseSink](hrallocadvisesink.md). La fonction **HrAllocAdviseSink** permet à ses appelant spécifier une fonction de rappel qui appelle **notifier** dans le cadre de la notification. La fonction de rappel est conforme au prototype [NOTIFCALLBACK](notifcallback.md) . Fonctions de rappel implémentées par les clients toujours retournent S_OK ; fonctions de rappel implémentées par les fournisseurs de service peuvent renvoyer CALLBACK_DISCONTINUE. 
  
Si une fonction de rappel renvoie CALLBACK_DISCONTINUE, MAPI arrête l’envoi de notifications et renvoie NOTIFY_CANCELED dans le paramètre _lpulFlags_ de la méthode **Notify** . Vous pouvez supposer que le processus est inactive et arrêter la génération de notifications pour ce processus. Si **Notify** renvoie la valeur 0 dans _lpulFlags_, le processus est toujours actif et vous pouvez continuer à envoyer des notifications, comme il convient.
  
Lorsque vous utilisez des notifications synchrones, veillez à éviter les situations de blocage.
  
Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [Notification](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propriété canonique PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport : IUnknown](imapisupportiunknown.md)

