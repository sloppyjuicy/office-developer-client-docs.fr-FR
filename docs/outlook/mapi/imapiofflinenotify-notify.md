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
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783890"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**S’applique à**: Outlook 
  
Envoie des notifications au client sur les modifications de l’état de connexion.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Paramètres

 _pNotifyInfo_
  
> [in] La notification qui envoie au client Outlook. La notification indique la partie de l’état de connexion qui a été modifié, l’état de connexion ancien et le nouvel état de connexion.
    
## <a name="remarks"></a>Remarques

Outlook utilise cette méthode pour envoyer les rappels de notification à un client. Pour que cette interface disponible pour Microsoft Outlook 2010 ou Microsoft Outlook 2013, le client doit implémenter cette interface et lui passer un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lorsque vous configurez des rappels à l’aide de **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**. 
  
Le client transfère également à **MAPIOFFLINE_ADVISEINFO** un jeton client que Outlook 2010 ou Outlook 2013 utilise **IMAPIOfflineNotify::Notify** pour identifier le client enregistré pour le rappel de notification. 
  
En règle générale, Outlook 2010 et Outlook 2013 peuvent informer un client de modifications en ligne/hors connexion et les autres changements d’état de connexion, mais l’API d’état en mode hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion. Le client doit ignorer toutes les autres notifications.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état en mode hors connexion](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

