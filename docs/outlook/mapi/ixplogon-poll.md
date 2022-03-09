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
ms.openlocfilehash: 2528c6d397198b6445caf7d5d3dcb1cdd1705a66
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368586"
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

Lepooler MAPI appelle régulièrement la méthode **IXPLogon::P élément** si le fournisseur de transport indique qu’il doit être interrogé pour de nouveaux messages, ce que le fournisseur fait en passant l’indicateur LOGON_SP_POLL à l’appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) au début d’une session. Si le fournisseur de transport indique en réponse à l’appel de sondage qu’un ou plusieurs messages entrants sont disponibles pour le traitement, lepooler MAPI appelle la méthode [IXPLogon::StartMessage](ixplogon-startmessage.md) pour permettre au fournisseur de traiter le premier message entrant. Le fournisseur de transport indique les messages entrants en fixant la valeur du paramètre _lpulIncoming_ sur une valeur autre que zéro. 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

