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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783645"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**S’applique à**: Outlook 
  
Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Un numéro de connexion qui représente l’inscription d’être annulée. Le paramètre _ulConnection_ doit contenir une valeur renvoyée par un appel précédent à la méthode [IAddrBook::Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’enregistrement a été annulée.
    
## <a name="remarks"></a>Remarques

Clients appellent la méthode **Unadvise** pour arrêter de recevoir des notifications sur les modifications apportées à une entrée de carnet d’adresses particulière. Lorsqu’un enregistrement de notification est annulé, le carnet d’adresses versions fournisseur son pointeur vers l’appelant de notification récepteur. Toutefois, la version peut se produire lors de l’appel **Unadvise** ou ultérieurement, si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . Lorsqu’une notification est en cours, la version est différée jusqu'à ce que la méthode **OnNotify** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

