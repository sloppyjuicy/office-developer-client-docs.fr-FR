---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329469"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule une inscription pour les notifications avec une visionneuse de formulaires précédemment établie en appelant [IMAPIForm:: Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> dans Numéro de connexion qui identifie l'enregistrement de notification à annuler.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'inscription a été annulée.
    
E_INVALIDARG 
  
> Le numéro de connexion transmis dans le paramètre _ulConnection_ ne représente pas une inscription valide. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIForm::** Unadvise pour annuler une inscription pour la notification qu'elles ont été initialement établies en appelant la méthode **IMAPIForm:: Advise** . 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Ignorez le pointeur que vous tenez au récepteur de notification d'affichage de la visionneuse de formulaires en appelant sa méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . En règle générale, la **publication** est appelée pendant l'appel Unadvise. **** Toutefois, si un autre thread appelle l'une des méthodes [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) pour le récepteur de notifications d'affichage, retardez l'appel de **libération** jusqu'à ce que la méthode **IMAPIViewAdviseSink** soit renvoyée. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

