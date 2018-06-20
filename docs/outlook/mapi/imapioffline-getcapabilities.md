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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 205c9dd28692592ddf133b1b30989ba9fd4236f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783858"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**S’applique à**: Outlook 
  
Obtient les conditions pour lequel les rappels sont pris en charge par un objet en mode hors connexion.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Paramètres

 _pulCapablities_
  
> [out] Un masque de bits des indicateurs de capacité suivants :
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> L’objet en mode hors connexion est capable de fournir des notifications en mode hors connexion.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> L’objet en mode hors connexion est capable de fournir des notifications en ligne.
    
## <a name="remarks"></a>Remarques

À l’ouverture d’un objet en mode hors connexion à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client peut interroger sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) pour obtenir un pointeur vers une interface **IMAPIOffline** et **IMAPIOffline::GetCapabilities** pour découvrir les rappels pris en charge des appels par l’objet. Le client peut ensuite choisir configurer des rappels à l’aide de **IMAPIOfflineMgr**.
  
Notez que, selon le serveur de messagerie pour un objet en mode hors connexion, un objet qui prend en charge des rappels pour passer en ligne ne prend pas nécessairement en charge des rappels pour passer en mode hors connexion.
  
Notez également que, pendant un objet en mode hors connexion peut prendre en charge des rappels pour que les modifications qu’en ligne/hors connexion, l’API d’état en mode hors connexion prend en charge uniquement les modifications en ligne/hors connexion et les clients doivent vérifier pour seulement ces fonctionnalités.
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

