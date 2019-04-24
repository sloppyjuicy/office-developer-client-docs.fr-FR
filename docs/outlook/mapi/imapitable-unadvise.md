---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328804"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule l'envoi des notifications précédemment configurées avec un appel à la méthode [IMAPITable:: Advise](imapitable-advise.md) . 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> dans Numéro de la connexion d'inscription renvoyée par un appel de la procédure [IMAPITable:: Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMAPITable::** Unadvise pour libérer le pointeur vers l'objet de récepteur de notifications transmis dans le paramètre _lpAdviseSink_ de l'appel précédent à **IMAPITable:: Advise**, ce qui a pour effet d'annuler une inscription aux notifications. Dans le cadre du rejet du pointeur vers l'objet de récepteur de notification, la méthode **IUnknown:: Release** de l'objet est appelée. En règle générale, la **publication** est appelée pendant l'appel Unadvise, mais si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour le récepteur de notifications, l'appel de **libération** est retardé jusqu'à ce que l' **OnNotify** **** méthode renvoie. 
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). Pour obtenir des informations spécifiques sur la notification de table, consultez la rubrique [à propos des notifications de table](about-table-notifications.md). Pour plus d'informations sur l'utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez la rubrique [prise en](supporting-event-notification.md)charge des notifications d'événements.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: NotificationOff  <br/> |MFCMAPI utilise la méthode **IMAPITable::** Unadvise pour annuler les notifications pour le tableau.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

