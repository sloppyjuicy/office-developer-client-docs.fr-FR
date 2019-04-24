---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328958"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre un récepteur de notifications pour recevoir des notifications via MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _lpKey_
  
> dans Pointeur vers une clé de notification qui représente l'objet de source Advise. Le paramètre _lpKey_ ne peut pas être null. 
    
 _ulEventMask_
  
> dans Masque de valeurs qui indiquent les types d'événements de notification qui intéressent l'appelant et qui doit être inclus dans l'inscription. Les valeurs suivantes sont valides:
    
 _fnevCriticalError_
  
> Enregistre les notifications concernant les erreurs graves, telles que la mémoire insuffisante.
    
 _fnevExtended_
  
> Enregistre les notifications relatives aux événements spécifiques au carnet d'adresses ou au fournisseur de banque de messages particulier.
    
 _fnevNewMail_
  
> Enregistre les notifications relatives à l'arrivée de nouveaux messages. 
    
 _fnevObjectCreated_
  
> Enregistre les notifications relatives à la création d'un nouvel objet.
    
 _fnevObjectCopied_
  
> Enregistre les notifications relatives à un objet en cours de copie.
    
 _fnevObjectDeleted_
  
> Enregistre les notifications relatives à la suppression d'un objet.
    
 _fnevObjectModified_
  
> Enregistre les notifications relatives à un objet modifié.
    
 _fnevObjectMoved_
  
> Enregistre les notifications relatives à un objet déplacé.
    
 _fnevSearchComplete_
  
> Enregistre les notifications relatives à l'exécution d'une opération de recherche.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le fonctionnement de la notification. L'indicateur suivant peut être défini:
    
NOTIFY_SYNC 
  
> Lorsque l'appelant appelle la méthode [IMAPISupport:: Notify](imapisupport-notify.md) pour générer des notifications pour ce récepteur de notifications, **Notify** doit effectuer tous les appels nécessaires pour informer les récepteurs avant de renvoyer. Si cet indicateur n'est pas défini, la notification est asynchrone et les rappels sont mis en file d'attente vers les processus qui sont abonnés et démarrés lorsque ces processus acquièrent le contrôle de l'UC. 
    
 _lpAdviseSink_
  
> dans Pointeur vers un objet de récepteur de notifications. 
    
 _lpulConnection_
  
> remarquer Pointeur vers un numéro de connexion différent de zéro qui représente l'inscription.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'enregistrement de la notification a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: subscribe** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services appellent **s'abonner** à partir de l'une de leurs méthodes de **Conseil** pour permettre à MAPI de gérer les notifications. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour utiliser les méthodes de prise en charge de MAPI pour la notification, créez une clé pour la source de notification l'objet sur lequel les notifications doivent être générées. La valeur de la clé doit être unique et doit être régénérée facilement chaque fois que l'objet est modifié. 
  
MAPI utilise la clé de notification pour rechercher toutes les fonctions de rappel enregistrées via la fonction [HrAllocAdviseSink](hrallocadvisesink.md) pour la source de notification correspondante. TransMettez cette clé à **IMAPISupport:: Notify** chaque fois que vous devez générer une notification pour la source d'avertissement correspondante. 
  
L'indicateur NOTIFY_SYNC affecte l'opération des appels suivants à **notifier**. Lorsque vous définissez NOTIFY_SYNC, **** la notification n'est pas renvoyée tant qu'elle n'a pas terminé d'envoyer toutes les notifications nécessaires. Lorsque vous ne définissez pas NOTIFY_SYNC, la fonctionnalité **Notify** fonctionne de manière asynchrone, éventuellement en retour avant l'envoi de toutes les notifications. 
  
## <a name="see-also"></a>Voir aussi



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notification](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

