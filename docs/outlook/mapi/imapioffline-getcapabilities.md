---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433373"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient les conditions pour lesquelles les rappels sont pris en charge par un objet hors connexion.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Paramètres

 _pulCapablities_
  
> remarquer Masque de masque des indicateurs de fonctionnalité suivants:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> L'objet hors connexion est capable de fournir des notifications hors connexion.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> L'objet hors connexion est capable de fournir des notifications en ligne.
    
## <a name="remarks"></a>Remarques

Lors de l'ouverture d'un objet hors connexion à l'aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client peut effectuer une requête sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) pour obtenir un pointeur vers une interface **IMAPIOffline** et appeler **IMAPIOffline:: GetCapabilities** pour connaître les rappels pris en charge par l'objet. Le client peut ensuite choisir de configurer les rappels à l'aide de **IMAPIOfflineMgr**.
  
Notez que, en fonction du serveur de messagerie d'un objet hors connexion, un objet qui prend en charge les rappels de mise en ligne ne prend pas nécessairement en charge les rappels pour le passage en mode hors connexion.
  
Notez également que, bien qu'un objet hors connexion puisse prendre en charge des rappels pour les modifications autres que Online/Offline, l'API d'État hors connexion prend en charge uniquement les modifications en ligne/hors connexion, et les clients doivent vérifier uniquement ces fonctionnalités.
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

