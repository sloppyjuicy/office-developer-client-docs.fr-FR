---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2321489893d8f085931d4dcb61e4688750c9a8ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621016"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule l’inscription des notifications auprès d’une visionneuse de formulaires précédemment établie en appelant [IMAPIForm::Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulConnection_
  
> [in] Numéro de connexion qui identifie l’inscription de notification à annuler.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a été annulée.
    
E_INVALIDARG 
  
> Le numéro de connexion transmis dans le  _paramètre ulConnection_ ne représente pas une inscription valide. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIForm::Unadvise** pour annuler une inscription pour la notification qu’elles ont d’abord établie en appelant la méthode **IMAPIForm::Advise.** 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Ignorer le pointeur que vous maintenez dans la vue de la visionneuse de formulaires pour le conseiller en appelant sa méthode [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) En règle générale, **Release** est appelé pendant **l’appel Unadvise.** Toutefois, si un autre thread est en train d’appeler l’une des méthodes [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) pour le sink de conseil d’affichage, retardez l’appel release jusqu’à ce que la méthode **IMAPIViewAdviseSink** renvoie.  
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

