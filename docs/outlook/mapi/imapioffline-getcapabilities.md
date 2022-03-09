---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
ms.openlocfilehash: 0c5068e8cca5548e54641fe9ee66c168e75db9e9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375901"
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

 _tamponscapablities_
  
> [out] Masque de bits des indicateurs de fonctionnalité suivants :
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> L’objet hors connexion est capable de fournir des notifications hors connexion.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> L’objet hors connexion est capable de fournir des notifications en ligne.
    
## <a name="remarks"></a>Remarques

Lors de l’ouverture d’un objet hors connexion à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client peut interroger [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) pour obtenir un pointeur vers une interface **IMAPIOffline** et appeler **IMAPIOffline::GetCapabilities** pour connaître les rappels pris en charge par l’objet. Le client peut ensuite choisir de configurer des rappels à l’aide **d’IMAPIOfflineMgr**.
  
Notez que, selon le serveur de messagerie d’un objet hors connexion, un objet qui prend en charge les rappels pour la mise en ligne ne prend pas nécessairement en charge les rappels pour la mise hors connexion.
  
Notez également que, bien qu’un objet hors connexion puisse prendre en charge les rappels pour les modifications autres que celles en ligne/hors connexion, l’API d’état hors connexion prend uniquement en charge les modifications en ligne/hors connexion, et les clients doivent vérifier uniquement ces fonctionnalités.
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

