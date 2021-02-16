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
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419925"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit un réception de notification pour recevoir des notifications via MAPI.
  
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
  
> [in] Pointeur vers une clé de notification qui représente l’objet source de notification. Le  _paramètre lpKey_ ne peut pas être NULL. 
    
 _ulEventMask_
  
> [in] Masque de valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et qui doivent être inclus dans l’inscription. Les valeurs suivantes sont valides :
    
 _fnevCriticalError_
  
> S’inscrit aux notifications concernant les erreurs graves, telles que la mémoire insuffisante.
    
 _fnevExtended_
  
> S’inscrit aux notifications sur les événements spécifiques au carnet d’adresses ou au fournisseur de magasin de messages particulier.
    
 _fnevNewMail_
  
> S’inscrit aux notifications concernant l’arrivée de nouveaux messages. 
    
 _fnevObjectCreated_
  
> S’inscrit aux notifications concernant la création d’un nouvel objet.
    
 _fnevObjectCopied_
  
> S’inscrit aux notifications concernant un objet en cours de copie.
    
 _fnevObjectDeleted_
  
> S’inscrit aux notifications concernant un objet en cours de suppression.
    
 _fnevObjectModified_
  
> S’inscrit aux notifications concernant un objet modifié.
    
 _fnevObjectMoved_
  
> S’inscrit aux notifications concernant un objet déplacé.
    
 _fnevSearchComplete_
  
> S’inscrit aux notifications concernant la fin d’une opération de recherche.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le fonctionnement de la notification. L’indicateur suivant peut être définie :
    
NOTIFY_SYNC 
  
> Lorsque l’appelant appelle la méthode [IMAPISupport::Notify](imapisupport-notify.md) pour générer des notifications pour ce réception de notification, **Notify** doit effectuer tous les appels nécessaires pour avertir les réceptions avant de revenir. Si cet indicateur n’est pas définie, la notification est asynchrone et les rappels sont mis en file d’attente aux processus abonnés et démarrés lorsque ces processus ont le contrôle de l’UC. 
    
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de sink de conseil. 
    
 _lpulConnection_
  
> [out] Pointeur vers un numéro de connexion autre que zéro qui représente l’inscription.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de la notification a réussi.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::Subscribe** est implémentée pour tous les objets de support du fournisseur de services. Les fournisseurs de services **appellent Subscribe** à partir de l’une de leurs **méthodes Advise** pour permettre à MAPI de gérer les notifications. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour utiliser les méthodes de prise en charge MAPI pour la notification, créez une clé pour la source de notifications sur l’objet sur lequel les notifications doivent être générées. La valeur de la clé doit être unique et être facilement régénérée chaque fois que l’objet change. 
  
MAPI utilise la clé de notification pour rechercher les fonctions de rappel enregistrées via la fonction [HrAllocAdviseSink](hrallocadvisesink.md) pour la source de notification correspondante. Passez cette clé à **IMAPISupport::Notify** chaque fois que vous devez générer une notification pour la source de notification correspondante. 
  
L NOTIFY_SYNC’indicateur affecte le fonctionnement des appels ultérieurs à **Notify**. Lorsque vous définissez NOTIFY_SYNC, **Notify** ne renvoie pas tant qu’il n’a pas terminé d’envoyer toutes les notifications nécessaires. Lorsque vous ne définissez pas NOTIFY_SYNC, **Notify** fonctionne de manière asynchrone, éventuellement avant l’envoi de toutes les notifications. 
  
## <a name="see-also"></a>Voir aussi



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notification](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

