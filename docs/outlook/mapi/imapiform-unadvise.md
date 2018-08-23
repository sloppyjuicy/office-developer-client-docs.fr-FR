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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 33287d8ac6b1faeba8b8746a95850f6fd1c37462
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579486"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Annule une inscription pour les notifications avec une visionneuse de formulaire précédemment établie en appelant [IMAPIForm::Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Un numéro de connexion qui identifie l’enregistrement de notification d’être annulée.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’enregistrement a été annulée.
    
E_INVALIDARG 
  
> Le numéro de connexion passé dans le paramètre _ulConnection_ ne représente pas un enregistrement valid. 
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIForm::Unadvise** pour annuler une inscription pour la notification qui ils tout d’abord établies en appelant la méthode **IMAPIForm::Advise** . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Ignorer le pointeur qui vous sont maintenant à l’affichage de l’utilisateur du formulaire de notification récepteur en appelant la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . En règle générale, la **version** est appelé pendant l’appel **Unadvise** . Toutefois, si un autre thread est en appelant une des méthodes [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) pour l’affichage de notification récepteur, différer l’appel de la **version** jusqu'à ce que la méthode **IMAPIViewAdviseSink** renvoie. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

