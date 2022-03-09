---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
ms.openlocfilehash: a20bead4672b5e863a30e2f65462acec1566d537
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376321"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le processus de ffage de logo.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le processus de ffage de logo a été lancé avec succès.
    
## <a name="remarks"></a>Remarques

Le processus de ffage de session est généralement démarré lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) pour mettre fin à une session. MAPI appelle ensuite la méthode **IABLogon::Logoff** de chaque fournisseur de carnet d’adresses pour démarrer le processus de désabonnement. 
  
La **méthode IABLogon::Logoff** : 
  
- Libère tous les objets ouverts, tels que les sous-objets ou l’objet d’état.
    
- Libère l’objet de support du fournisseur.
    
Pour plus d’informations sur le processus de fermeture de logo des fournisseurs de carnets d’adresses, voir [Shutting Down a Service Provider](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

