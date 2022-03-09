---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
ms.openlocfilehash: fff2a3097833006ae895a2c8a9faf776f72a532e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378029"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule l’envoi de notifications précédemment définies avec un appel à la [méthode IMsgStore::Advise](imsgstore-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Numéro de connexion associé à un enregistrement de notification actif. La valeur  _de ulConnection_ doit avoir été renvoyée par un appel précédent à la **méthode IMsgStore::Advise** . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a été annulée.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::Unadvise** annule l’inscription à la notification. **Unadvise relâche** son pointeur vers le réception de conseil de l’appelant, qu’il a reçu dans l’appel **De** conseil utilisé pour l’inscription. 
  
En règle **générale, Unadvise** appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du sink de conseil pendant l’appel **Unadvise** . Toutefois, si un autre thread est en train d’appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de conseil, l’appel de publication est différé jusqu’à ce que la méthode **OnNotify** soit de retour. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

