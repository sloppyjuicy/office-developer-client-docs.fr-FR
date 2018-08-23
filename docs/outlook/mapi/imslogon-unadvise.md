---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4ee17799fc42faf383461af7eed9d700d17b868e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582384"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Supprime l’inscription d’un objet pour la notification des modifications de banque de messages précédemment établie à l’aide d’un appel à la méthode [IMSLogon::Advise](imslogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Le numéro de la connexion d’enregistrement renvoyé par un appel à **IMSLogon::Advise**.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La méthode **IMSLogon::Unadvise** pour libérer le pointeur vers l’objet de récepteur advise transmis dans le paramètre _lpAdviseSink_ dans l’appel précédent à **IMSLogon::Advise**, annulant ainsi une notification implémentés par les fournisseurs la base de messages inscription. Dans le cadre d’ignorer le pointeur vers l’objet de récepteur advise, la méthode l’objet [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) est appelée. En règle générale, la **version** est appelé pendant l’appel **Unadvise** . Toutefois, si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise, l’appel de la **version** est différé jusqu'à ce que la méthode **OnNotify** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

