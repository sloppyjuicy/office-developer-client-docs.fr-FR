---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e06f78317a1e98d47a37cb7059042b254567fe8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573683"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Un numéro de connexion qui représente l’inscription d’être annulée. Le paramètre _ulConnection_ doit contenir une valeur renvoyée par un appel précédent à la méthode [IAddrBook::Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’enregistrement a été annulée.
    
## <a name="remarks"></a>Remarques

Clients appellent la méthode **Unadvise** pour arrêter de recevoir des notifications sur les modifications apportées à une entrée de carnet d’adresses particulière. Lorsqu’un enregistrement de notification est annulé, le carnet d’adresses versions fournisseur son pointeur vers l’appelant de notification récepteur. Toutefois, la version peut se produire lors de l’appel **Unadvise** ou ultérieurement, si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . Lorsqu’une notification est en cours, la version est différée jusqu'à ce que la méthode **OnNotify** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

