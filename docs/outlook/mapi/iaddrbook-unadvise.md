---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
ms.openlocfilehash: 1a501c52b59a3640274dc0598fad83be6477b372
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382124"
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
  
> [in] Numéro de connexion qui représente l’inscription à annuler. Le  _paramètre ulConnection_ doit contenir une valeur renvoyée par un appel préalable à la [méthode IAddrBook::Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a été annulée.
    
## <a name="remarks"></a>Remarques

Les clients appellent **la méthode Unadvise** pour arrêter de recevoir des notifications concernant les modifications apportées à une entrée de carnet d’adresses particulière. Lorsqu’une inscription de notification est annulée, le fournisseur de carnet d’adresses relâche son pointeur vers le sink de notification de l’appelant. Toutefois, la publication peut se produire pendant l’appel **Unadvise** ou à un moment ultérieur, si un autre thread est en cours d’appel de la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . Lorsqu’une notification est en cours, la publication est retardée jusqu’au retour de la méthode **OnNotify** . 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

