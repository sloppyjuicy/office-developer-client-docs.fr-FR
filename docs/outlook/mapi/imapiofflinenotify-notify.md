---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410692"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Envoie des notifications au client concernant les modifications apportées à l’état de connexion.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parameters

 _pNotifyInfo_
  
> [in] Notification Outlook au client. La notification indique la partie de l’état de connexion qui a changé, l’ancien état de connexion et le nouvel état de connexion.
    
## <a name="remarks"></a>Remarques

Outlook utilise cette méthode pour envoyer des rappels de notification à un client. Pour rendre cette interface disponible pour Microsoft Outlook 2010 ou Microsoft Outlook 2013, le client doit implémenter cette interface et lui transmettre un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lors de la configuration des rappels à l’aide **[d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
  
Le client passe également à **MAPIOFFLINE_ADVISEINFO** un jeton client que Outlook 2010 ou Outlook 2013 utilise dans **IMAPIOfflineNotify::Notify** pour identifier le client inscrit pour le rappel de notification. 
  
En règle générale, Outlook 2010 et Outlook 2013 peuvent notifier un client de modifications en ligne/hors connexion et d’autres modifications d’état de connexion, mais l’API d’état hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion. Le client doit ignorer toutes les autres notifications.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

