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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a20fdd45c39cc2147f8fdc7b1998ff6d1b0797bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586206"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le processus de fermeture de session.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le processus de fermeture de session a été lancé.
    
## <a name="remarks"></a>Remarques

Le processus de déconnexion est généralement démarré lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) pour mettre fin à une session. MAPI appelle ensuite la méthode **IABLogon::Logoff** de chaque fournisseur carnet d’adresses pour démarrer le processus de fermeture de session. 
  
La méthode **IABLogon::Logoff** effectue les opérations suivantes : 
  
- Libère tous les objets, tels que les sous-objets ou l’objet d’état.
    
- Libère l’objet de prise en charge du fournisseur.
    
Pour plus d’informations sur le processus de déconnexion de fournisseurs de carnet d’adresses, voir [Arrêt vers le bas un fournisseur de services](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

