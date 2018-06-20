---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784499"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**S’applique à**: Outlook 
  
Indique que le système est inactif, l’activation du fournisseur de transport effectuer des opérations de priorité basse.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle régulièrement la méthode **IXPLogon::Idle** , si vous y êtes invité, pendant les heures lorsque le système est inactif en transmettant l’indicateur XP_LOGON_SP dans l’appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) qui a ouvert la session en cours. Lorsque le système est inactif, le fournisseur de transport peut effectuer des opérations en arrière-plan qui ne sont pas appropriés pendant les autres appels, ou qui ont besoin de se produire à intervalles réguliers. 
  
## <a name="see-also"></a>Voir aussi



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

