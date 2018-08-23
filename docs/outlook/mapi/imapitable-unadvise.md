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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7de4d3c58d5eeefcf9a82235333da5db4703bc8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592975"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMAPITable::Advise](imapitable-advise.md) . 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Le numéro de la connexion d’enregistrement renvoyé par un appel à [IMAPITable::Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMAPITable::Unadvise** pour libérer le pointeur vers l’objet de récepteur advise transmis dans le paramètre _lpAdviseSink_ dans l’appel précédent à **IMAPITable::Advise**, annulant ainsi un enregistrement de notification. Dans le cadre d’ignorer le pointeur vers l’objet de récepteur advise, la méthode l’objet **IUnknown::Release** est appelée. En règle générale, la **version** est appelé pendant l’appel **Unadvise** , mais si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour le récepteur de notifications, l’appel de la **version** est différée jusqu'à **OnNotify** méthode retourne. 
  
Pour plus d’informations sur le processus de notification, voir [Notification d’événement MAPI](event-notification-in-mapi.md). Pour obtenir des informations spécifiques sur la notification de la table, voir [Sur les Notifications de Table](about-table-notifications.md). Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Prise en charge de Notification d’événement](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI utilise la méthode **IMAPITable::Unadvise** pour annuler des notifications pour la table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

