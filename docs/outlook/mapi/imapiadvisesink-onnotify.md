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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783681"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**S’applique à**: Outlook 
  
Répond à une notification en effectuant une ou plusieurs tâches. Les tâches exécutées varient selon le type d’événement et l’objet qui génère la notification. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Paramètres

 _cNotif_
  
> [in] Le nombre de structures [NOTIFICATION](notification.md) indiqué par le paramètre _lpNotifications_ . 
    
 _lpNotifications_
  
> [in] Pointeur vers une ou plusieurs structures **NOTIFICATION** qui fournissent des informations sur les événements qui se sont produites. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La notification a été correctement traitée.
    
## <a name="remarks"></a>Remarques

Le processus de notification démarre lorsqu’un client ou un MAPI effectue un appel à la méthode **Advise** d’un fournisseur de services pour s’inscrire pour recevoir une notification d’un type particulier d’un objet particulier. L’un des paramètres à la méthode **Advise** est un pointeur vers un objet récepteur advise qui implémente l’interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Lorsqu’un événement se produit à l’objet cible qui correspond à la notification inscrit, le fournisseur de services, directement ou indirectement via MAPI, appelle **OnNotify** (méthode) du récepteur advise. 
  
L’appel de **OnNotify** peut se produire lors de l’appel MAPI qui est à l’origine de l’événement ou ultérieurement. Sur les systèmes qui prennent en charge plusieurs threads d’exécution, **OnNotify** peut être appelée sur le même thread qui a été utilisé pour l’enregistrement ou sur un autre thread. Les clients peuvent s’assurer que l’appel de **OnNotify** est effectué sur le même thread utilisé pour appeler **Advise** en créant le récepteur de notifications qu’elles passent à **Advise** avec la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Le paramètre _lpNotifications_ pointe vers une ou plusieurs structures **NOTIFICATION** qui décrivent ce qui a changé pendant l’événement. Il existe un autre type de structure de **NOTIFICATION** pour chaque type d’événement. 
  
Le tableau suivant répertorie les valeurs qui sont utilisées pour représenter les types d’événements et les structures associés à chaque valeur possibles :
  
|**Type d’événement notification**|**Structure correspondante**|
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
   
Pour plus d’informations sur la façon de configurer et d’arrêter les notifications, consultez les entrées de référence pour les méthodes **Advise** et **Unadvise** pour une des interfaces suivantes : [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)et [IMSLogon](imslogoniunknown.md). 
  
Pour obtenir des informations générales sur le processus de notification, voir [Notification d’événement MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Votre implémentation **OnNotify** consiste à un ou plusieurs blocs de code pour chaque type de notification que vous souhaitez recevoir. Dans ces blocs de code, effectuez toutes les tâches que vous prenez en compte nécessaire en réponse à la notification. Par exemple, supposons que vous inscrivez pour recevoir des notifications **fnevObjectModified** dans un dossier qui est inclus dans l’affichage d’une boîte de dialogue. Dans le bloc de code que vous incluez dans votre méthode **OnNotify** pour gérer les notifications **fnevObjectModified** , vous pouvez envoyer un message Windows à la boîte de dialogue pour demander un affichage mis à jour. 
  
Ne modifiez pas ou ne libérer la structure **NOTIFICATION** transmise à **OnNotify**. Les données de la structure sont valides uniquement jusqu'à **OnNotify** renvoie. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

En cas de modifications apportées à plusieurs objets, vous pouvez signaler un récepteur de notifications enregistrés dans un seul appel à **OnNotify** ou dans plusieurs appels en fonction des contraintes de mémoire. Cela est vrai, même si les modifications sont le résultat d’un appel de méthode ou plusieurs. Par exemple, un appel à [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) peut affecter plusieurs dossiers et messages. Comme un fournisseur de magasins de message, vous pouvez appeler **OnNotify** avec un type d’événement **fnevObjectModified** pour le dossier cible ou un grand nombre d’appels, un pour chaque affectent les messages. De même, si un client effectue des appels répétés à [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), ces appels peuvent être combinées dans un événement **fnevObjectModified** pour le dossier ou séparés en événements individuels **fnevObjectCreated** pour chaque nouveau message. 
  
Pour plus d’informations sur la façon et le moment générer des notifications, voir [Notification d’événement MAPI](event-notification-in-mapi.md) et [Prenant en charge les notifications](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AdviseSink.h et AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |La classe CAdviseSink est implémentée pour gérer toutes les notifications de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Notification](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

