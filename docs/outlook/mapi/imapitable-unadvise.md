---
title: IMAPITableUnadvise
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aad37ed77d90745f0fb6f58df1dfbf9303648494
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770751"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule l’envoi de notifications précédemment définies avec un appel à la [méthode IMAPITable::Advise](imapitable-advise.md) . 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Numéro de la connexion d’inscription renvoyée par un appel [à IMAPITable::Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMAPITable::Unadvise** pour libérer le pointeur vers l’objet de réception de notification transmis dans le paramètre _lpAdviseSink_ dans l’appel précédent à **IMAPITable::Advise**, ce qui annule l’inscription d’une notification. Dans le cadre de l’ignorer, la méthode **IUnknown::Release** de l’objet est appelée. En règle générale, **Release** est appelé pendant l’appel **Unadvise** , mais si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour le sink de conseil, l’appel **de** publication est retardé jusqu’à ce que la méthode **OnNotify** renvoie. 
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur les notifications de tableau, voir [À propos des notifications de tableau](about-table-notifications.md). Pour plus d’informations sur l’utilisation **des méthodes IMAPISupport** pour prendre en charge la notification, voir [Notification d’événement de prise en charge](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI utilise la **méthode IMAPITable::Unadvise** pour annuler les notifications pour la table. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

