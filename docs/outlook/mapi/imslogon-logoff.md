---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399234"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournisseur de magasins de journaux d’un message. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in] Réservé ; doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs de banque de messages implémentent la méthode **IMSLogon::Logoff** pour forcer l’arrêt un fournisseur de magasin de message. **IMSLogon::Logoff** est appelée dans les situations suivantes : 
  
- Alors que MAPI se déconnecte un client après un appel à la méthode [IMAPISession::Logoff](imapisession-logoff.md) . 
    
- Alors que MAPI se déconnecte un fournisseur de magasin de message. Dans ce cas, **IMSLogon::Logoff** est appelée dans le cadre de MAPI de traitement de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de l’objet de prise en charge créés par le fournisseur de banque de messages pendant le traitement d’un [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ou un **IUnknown :: Version** appel de méthode sur un objet de banque de messages. 
    
## <a name="see-also"></a>Voir aussi



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

