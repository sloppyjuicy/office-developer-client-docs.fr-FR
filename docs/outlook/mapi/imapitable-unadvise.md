---
title: IMAPITableUnadvise
description: IMAPITable Unadvise annule l’envoi de notifications précédemment configurées avec un appel à la méthode IMAPITable Advise.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
ms.openlocfilehash: f9000a1c2445e92eba9731725ebaf0ea3aa8fe57
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827792"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMAPITable::Advise](imapitable-advise.md) . 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _Ulconnection_
  
> [in] Numéro de la connexion d’inscription retournée par un appel à [IMAPITable::Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMAPITable::Unadvise** pour libérer le pointeur vers l’objet récepteur conseiller passé dans le paramètre _lpAdviseSink_ dans l’appel précédent à **IMAPITable::Advise**, annulant ainsi une inscription de notification. Dans le cadre de l’abandon du pointeur vers l’objet récepteur conseiller, la méthode **IUnknown::Release** de l’objet est appelée. En règle générale, **Release** est appelé pendant l’appel **non supervisé** , mais si un autre thread est en cours d’appel de la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour le récepteur conseiller, l’appel **release** est retardé jusqu’à ce que la méthode **OnNotify** retourne. 
  
Pour plus d’informations sur le processus de notification, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur la notification de table, consultez [À propos des notifications de table](about-table-notifications.md). Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez [Notification d’événement de prise en charge](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI utilise la méthode **IMAPITable::Unadvise** pour annuler les notifications pour la table. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

