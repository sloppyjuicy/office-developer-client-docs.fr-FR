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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: beeca6ba958c38e12fba7dbc2884c81e58bdf3c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590119"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre un récepteur de notifications pour recevoir des notifications par le biais de MAPI.
  
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
  
> [in] Pointeur vers une clé de notification qui représente l’objet source de notification. Le paramètre _lpKey_ ne peut pas être NULL. 
    
 _ulEventMask_
  
> [in] Un masque des valeurs qui indiquent les types d’événements de notification que l’appelant est intéressée par et doit être inclus dans l’enregistrement. Les valeurs suivantes sont valides :
    
 _fnevCriticalError_
  
> Enregistre les notifications sur les erreurs graves, telles que la mémoire insuffisante.
    
 _fnevExtended_
  
> Fournisseur de magasins registres pour les notifications concernant les événements spécifiques pour le carnet d’adresses ou le message.
    
 _fnevNewMail_
  
> Enregistre les notifications relatives à l’arrivée de nouveaux messages. 
    
 _fnevObjectCreated_
  
> Enregistre les notifications concernant la création d’un nouvel objet.
    
 _fnevObjectCopied_
  
> Enregistre les notifications relatives à un objet en cours de copie.
    
 _fnevObjectDeleted_
  
> Enregistre les notifications relatives à un objet en cours de suppression.
    
 _fnevObjectModified_
  
> Enregistre les notifications relatives à un objet en cours de modification.
    
 _fnevObjectMoved_
  
> Enregistre les notifications relatives à un objet en cours de déplacement.
    
 _fnevSearchComplete_
  
> Enregistre les notifications relatives à la fin d’une opération de recherche.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la notification se produit. Vous pouvez définir l’indicateur suivant :
    
NOTIFY_SYNC 
  
> Lorsque l’appelant appelle la méthode [IMAPISupport::Notify](imapisupport-notify.md) pour générer des notifications pour ce récepteur de notifications, **notifier** doivent effectuer tous les appels nécessaires pour informer les récepteurs avant de retourner. Si cet indicateur n’est pas défini, la notification est asynchrone et rappels sont en attente pour les processus qui ont souscrit et démarré lorsque ces processus prendre le contrôle de l’UC. 
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de réception de notifications. 
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro de connexion différente de zéro qui représente l’enregistrement.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de notification a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::Subscribe** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services à partir d’une des méthodes de leur **Advise** permettant de MAPI gérer les notifications d’appel **s’abonner** . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour utiliser les méthodes de prise en charge MAPI pour les notifications, créez une clé pour la source advise de l’objet sur les notifications doit être généré. La valeur de la clé doit être unique et doit être facilement régénérée chaque modification de l’objet. 
  
MAPI utilise la clé de notification pour rechercher des fonctions de rappel enregistrées par le biais de la fonction [HrAllocAdviseSink](hrallocadvisesink.md) pour la source advise correspondant. Passez cette clé à **IMAPISupport::Notify** chaque fois que vous devez générer une notification pour la source advise correspondante. 
  
L’indicateur NOTIFY_SYNC affecte le fonctionnement des appels ultérieurs à **notifier**. Lorsque vous définissez NOTIFY_SYNC, **notifier** ne retourne pas jusqu'à ce qu’il a terminé l’envoi de toutes les notifications nécessaires. Lorsque vous ne définissez pas NOTIFY_SYNC, **notifier** fonctionne de manière asynchrone, renvoyer avant toutes les notifications ont été envoyés. 
  
## <a name="see-also"></a>Voir aussi



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notification](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

