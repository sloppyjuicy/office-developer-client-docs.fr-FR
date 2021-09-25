---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f0981c87ccf51b98296d7658d5695b6c58d37948
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584205"
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
  
> [out] Valeur qui indique l’existence de messages entrants. Une valeur autre que zéro indique qu’il existe des messages entrants.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle régulièrement la méthode **IXPLogon::P élément** si le fournisseur de transport indique qu’il doit être interrogé pour de nouveaux messages, ce que le fournisseur fait en passant l’indicateur LOGON_SP_POLL à l’appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) au début d’une session. Si le fournisseur de transport  indique en réponse à l’appel de sondage qu’un ou plusieurs messages entrants peuvent être traitées, lepooler MAPI appelle la méthode [IXPLogon::StartMessage](ixplogon-startmessage.md) pour permettre au fournisseur de traiter le premier message entrant. Le fournisseur de transport indique les messages entrants en fixant la valeur du paramètre  _lpulIncoming_ sur une valeur autre que zéro. 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

