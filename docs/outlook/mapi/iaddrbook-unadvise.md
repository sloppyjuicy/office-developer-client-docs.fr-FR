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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286982"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule une inscription aux notifications précédemment établie pour une entrée de carnet d'adresses.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> dans Numéro de connexion qui représente l'inscription à annuler. Le paramètre _ulConnection_ doit contenir une valeur renvoyée par un appel antérieur à la méthode [IAddrBook:: Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'inscription a été annulée.
    
## <a name="remarks"></a>Remarques

Les clients appellent **** la méthode Unadvise pour cesser de recevoir des notifications sur les modifications apportées à une entrée de carnet d'adresses particulière. Lorsqu'une inscription aux notifications est annulée, le fournisseur de carnet d'adresses libère son pointeur vers le récepteur de notifications de l'appelant. Toutefois, la publication peut se produire pendant **** l'appel Unadvise ou ultérieurement, si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) . Lorsqu'une notification est en cours, la publication est retardée jusqu'à ce que la méthode **OnNotify** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

