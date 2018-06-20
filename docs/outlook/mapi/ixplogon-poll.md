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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784501"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**S’applique à**: Outlook 
  
Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Paramètres

 _lpulIncoming_
  
> [out] Une valeur qui indique la présence de messages entrants. Une valeur différente de zéro indique qu’il existe des messages entrants.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle régulièrement la méthode **IXPLogon::Poll** si le fournisseur de transport indique qu’il doit être interrogé pour les nouveaux messages, lequel le fournisseur signale à l’appel à [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) en transmettant le LOGON_SP_POLL méthode au début d’une session. Si le fournisseur de transport indique en réponse à l’appel de **sondage** qu’il y a un ou plus des messages entrants disponibles pour ce processus, le spouleur MAPI appelle la méthode [IXPLogon::StartMessage](ixplogon-startmessage.md) pour autoriser le fournisseur au processus de la première entrant Message. Le fournisseur de transport indique les messages entrants en définissant la valeur dans le paramètre _lpulIncoming_ sur une valeur différente de zéro. 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

