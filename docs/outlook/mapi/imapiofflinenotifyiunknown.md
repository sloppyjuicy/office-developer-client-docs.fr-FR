---
title: IMAPIOfflineNotify IUnknown
description: IMAPIOfflineNotifyIUnknown prend en charge Microsoft Outlook 2010 et Microsoft Outlook 2013 en envoyant des rappels de notification à un client.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
ms.openlocfilehash: de11d8d0e9aedb9317f4c2f788e22b412dd91f5e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816135"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge Microsoft Outlook 2010 et Microsoft Outlook 2013 lors de l’envoi de rappels de notification à un client.
  
|Propriété|Déscrption|
|:-----|:-----|
|Fourni par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[Notification](imapiofflinenotify-notify.md) <br/> |Envoie des notifications à un client concernant les modifications apportées à l’état de la connexion. |
   
## <a name="remarks"></a>Remarques

Le client doit implémenter cette interface et lui transmettre un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lors de la configuration des rappels à l’aide **[d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Par la suite, Outlook 2010 ou Outlook 2013 pourront utiliser cette interface pour envoyer des rappels de notification au client. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

