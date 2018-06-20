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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783596"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**S’applique à**: Outlook 
  
Lance le processus de fermeture de session.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

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

