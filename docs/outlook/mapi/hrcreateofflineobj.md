---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6a4f547ad55270eb3a2f4ec0ddb398c2d96fd257
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571940"
---
# <a name="hrcreateofflineobj"></a>HrCreateOfflineObj

**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Crée un objet MAPI hors connexion utilisé par le fournisseur et stocké afin d’avertir MAPI lorsque l’objet est en ligne et hors connexion. 
  
|||
|:-----|:-----|
|Exporté par :  <br/> |Msmapi32.dll  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Client  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> [in] Elle doit être 0.
    
_pCreateInfo_
  
> [in] Pointeur vers une structure **MAPIOFFLINE_CREATEINFO** qui contient les informations nécessaires pour créer l’objet hors connexion. 
    
_ppOffline_
  
> [out] Pointeur vers l’interface **IMAPIOfflineMgr.** 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
HrOpenOfflineObj
  
## <a name="example"></a>Exemple

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a>Voir aussi

- [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)
- [MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

