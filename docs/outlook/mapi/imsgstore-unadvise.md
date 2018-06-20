---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 516de39d721c532c003775bd366a52ed8144ab88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784287"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**S’applique à**: Outlook 
  
Annule l’envoi de notifications précédemment configurées avec un appel à la méthode [IMsgStore::Advise](imsgstore-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Le numéro de connexion associé à un enregistrement de notification actif. La valeur de _ulConnection_ doit avoir été renvoyée par un appel précédent à la méthode **IMsgStore::Advise** . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’enregistrement a été annulée.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::Unadvise** annule une inscription pour la notification. Versions **Unadvise** récepteur, à laquelle il a reçu l’appel **Advise** utilisées pour l’inscription de notification de son pointeur vers l’appelant. 
  
En règle générale, **Unadvise** appelle la méthode de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) du récepteur advise pendant l’appel **Unadvise** . Toutefois, si un autre thread est en cours de l’appel de méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

