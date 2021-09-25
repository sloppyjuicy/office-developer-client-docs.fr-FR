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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 229900a1d00b8764266c45795462deb470762eb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564203"
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

 _OleCapablities_
  
> [out] Masque de bits des indicateurs de fonctionnalité suivants :
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> L’objet hors connexion est capable de fournir des notifications hors connexion.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> L’objet hors connexion est capable de fournir des notifications en ligne.
    
## <a name="remarks"></a>Remarques

Lors de l’ouverture d’un objet hors connexion à l’aide de **[HrOpenOfflineObj,](hropenofflineobj.md)** un client peut interroger [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) pour obtenir un pointeur vers une interface **IMAPIOffline** et appeler **IMAPIOffline::GetCapabilities** pour rechercher les rappels pris en charge par l’objet. Le client peut ensuite choisir de configurer des rappels à l’aide **d’IMAPIOfflineMgr**.
  
Notez que, selon le serveur de messagerie d’un objet hors connexion, un objet qui prend en charge les rappels pour la mise en ligne ne prend pas nécessairement en charge les rappels pour la mise hors connexion.
  
Notez également que, bien qu’un objet hors connexion puisse prendre en charge les rappels pour les modifications autres que celles en ligne/hors connexion, l’API d’état hors connexion prend uniquement en charge les modifications en ligne/hors connexion, et les clients doivent vérifier uniquement ces fonctionnalités.
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

