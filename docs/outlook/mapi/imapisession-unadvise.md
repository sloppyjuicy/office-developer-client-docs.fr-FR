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
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335699"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule l’envoi de notifications précédemment définies avec un appel à la méthode [IMAPISession::Advise.](imapisession-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Numéro de connexion associé à un enregistrement de notification actif. La valeur de  _ulConnection doit_ avoir été renvoyée par un appel précédent à **IMAPISession::Advise**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a été annulée.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::Unadvise** annule l’inscription à la notification. **Unadvise relâche** son pointeur vers le réception de conseil de l’appelant, qu’il a reçu dans l’appel **De** conseil utilisé pour l’inscription. 
  
En règle **générale, Unadvise** appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du sink de conseil pendant l’appel **Unadvise.** Toutefois, si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de conseil, l’appel de publication est différé jusqu’à ce que la méthode **OnNotify** soit de retour.  
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

