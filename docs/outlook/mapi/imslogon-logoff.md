---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
ms.openlocfilehash: 3f86ec769ae1edbcb5c8e9f136196b933342ba40
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381746"
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

Les fournisseurs de magasins de messages implémentent **la méthode IMSLogon::Logoff** pour forcer l’arrêt d’un fournisseur de magasins de messages. **IMSLogon::Logoff** est appelé dans les situations suivantes : 
  
- Pendant que MAPI se dé connecte à un client après un appel à la méthode [IMAPISession::Logoff](imapisession-logoff.md) . 
    
- Pendant que MAPI se dé connecte à un fournisseur de magasins de messages. Dans ce cas, **IMSLogon::Logoff** est appelé dans le cadre du traitement MAPI de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de l’objet de support que le fournisseur de magasin de messages crée pendant qu’il traite un appel de méthode [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) **ou IUnknown::Release** sur un objet de magasin de messages. 
    
## <a name="see-also"></a>Voir aussi



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

