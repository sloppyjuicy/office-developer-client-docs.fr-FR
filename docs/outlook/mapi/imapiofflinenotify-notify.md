---
title: IMAPIOfflineNotifyNotify
description: Décrit la syntaxe, les paramètres et les remarques pour IMAPIOfflineNotifyNotify, qui envoie des notifications au client concernant les modifications apportées à l’état de la connexion.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
ms.openlocfilehash: b474caeb6a2f27d44dd17f803699a62418400426
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812094"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Envoie des notifications au client concernant les modifications apportées à l’état de la connexion.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Paramètres

 _pNotifyInfo_
  
> [in] Notification que Outlook envoie au client. La notification indique la partie de l’état de connexion qui a changé, l’ancien état de connexion et le nouvel état de connexion.
    
## <a name="remarks"></a>Remarques

Outlook utilise cette méthode pour envoyer des rappels de notification à un client. Pour rendre cette interface disponible pour Microsoft Outlook 2010 ou Microsoft Outlook 2013, le client doit implémenter cette interface et lui transmettre un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO lors de](mapioffline_adviseinfo.md)** la configuration des rappels à l’aide **[d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
  
Le client passe également à **MAPIOFFLINE_ADVISEINFO** un jeton client qui Outlook 2010 ou Outlook 2013 utilise dans **IMAPIOfflineNotify::Notify** pour identifier le client inscrit pour le rappel de notification. 
  
En général, Outlook 2010 et Outlook 2013 peuvent informer un client des modifications en ligne/hors connexion et d’autres changements d’état de connexion, mais l’API d’état hors connexion prend uniquement en charge les notifications pour les modifications en ligne/hors connexion. Le client doit ignorer toutes les autres notifications.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

