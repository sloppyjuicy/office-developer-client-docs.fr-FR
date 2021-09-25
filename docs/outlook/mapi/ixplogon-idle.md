---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d7a3b61760b21ee34d5726e9a321fd418c55d7ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613750"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique que le système est inactif, ce qui permet au fournisseur de transport d’effectuer des opérations de faible priorité.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle régulièrement la méthode **IXPLogon::Idle,** si nécessaire, lorsque le système est inactif en passant l’indicateur XP_LOGON_SP dans l’appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) qui a ouvert la session en cours. Lorsque le système est inactif, le fournisseur de transport peut effectuer des opérations en arrière-plan qui ne sont pas appropriées pendant d’autres appels ou qui doivent se produire régulièrement. 
  
## <a name="see-also"></a>Voir aussi



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

