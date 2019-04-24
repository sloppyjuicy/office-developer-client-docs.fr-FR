---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351610"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Paramètres

 _lpulIncoming_
  
> remarquer Valeur qui indique l'existence de messages entrants. Une valeur non nulle indique qu'il existe des messages entrants.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle régulièrement la méthode **IXPLogon::P oll** si le fournisseur de transport indique qu'il doit être interrogé pour de nouveaux messages, ce que fait le fournisseur en transmettant l'indicateur LOGON_SP_POLL à l'appel à l' [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) méthode au début d'une session. Si le fournisseur de transport indique en réponse à l'appel de **sondage** qu'il existe un ou plusieurs messages entrants qu'il est possible de traiter, le spouleur MAPI appelle la méthode [IXPLogon:: StartMessage](ixplogon-startmessage.md) pour permettre au fournisseur de traiter le premier Message. Le fournisseur de transport indique les messages entrants en définissant la valeur du paramètre _lpulIncoming_ sur une valeur différente de zéro. 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

