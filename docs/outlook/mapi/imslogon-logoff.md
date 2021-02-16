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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348873"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconnecte un fournisseur de magasins de messages. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in] Réservé ; doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de magasins de messages implémentent la méthode **IMSLogon::Logoff** pour forcer l’arrêt d’un fournisseur de magasins de messages. **IMSLogon::Logoff** est appelé dans les situations suivantes : 
  
- Pendant que MAPI se dé connecte à un client après un appel à la méthode [IMAPISession::Logoff.](imapisession-logoff.md) 
    
- Pendant que MAPI se dé connecte à un fournisseur de magasins de messages. Dans ce cas, **IMSLogon::Logoff** est appelé dans le cadre du traitement MAPI de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de l’objet de support que le fournisseur de magasin de messages crée pendant qu’il traite un appel de méthode [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) **ou IUnknown::Release** sur un objet de magasin de messages. 
    
## <a name="see-also"></a>Voir aussi



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

