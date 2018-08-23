---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3b582b48773b9f6f1a6f46f9c0e4c6dcb9782b86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592065"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMAPISession::Advise](imapisession-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Un numéro de connexion associé à un enregistrement de notification actif. La valeur de _ulConnection_ doit avoir été renvoyée par un appel précédent à **IMAPISession::Advise**.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’enregistrement a été annulée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::Unadvise** annule une inscription pour la notification. Versions **Unadvise** récepteur, à laquelle il a reçu l’appel **Advise** utilisées pour l’inscription de notification de son pointeur vers l’appelant. 
  
En règle générale, **Unadvise** appelle la méthode de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) du récepteur advise pendant l’appel **Unadvise** . Toutefois, si un autre thread est en cours de l’appel de méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

