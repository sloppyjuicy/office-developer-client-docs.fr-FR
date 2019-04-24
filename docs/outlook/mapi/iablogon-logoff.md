---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339297"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le processus de fermeture de session.
  
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
  
> Le processus de fermeture de session a été initié avec succès.
    
## <a name="remarks"></a>Remarques

Le processus de déconnexion est généralement démarré lorsqu'un client appelle la méthode [IMAPISession:: Logoff](imapisession-logoff.md) pour mettre fin à une session. MAPI appelle ensuite la méthode **IABLogon:: Logoff** du fournisseur de carnets d'adresses pour démarrer le processus de fermeture de session. 
  
La méthode **IABLogon:: Logoff** effectue les opérations suivantes: 
  
- Libère tous les objets ouverts, tels que les sous-objets ou l'objet d'État.
    
- Libère l'objet de prise en charge du fournisseur.
    
Pour plus d'informations sur le processus de fermeture de session des fournisseurs de carnets d'adresses, consultez la rubrique [arrêt d'un fournisseur de services](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

