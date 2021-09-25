---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a8a24d00aa9646d52f7409c1234eac12109075f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621009"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait une valeur qui indique si le contrôle de bouton est activé ou désactivé.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulState_
  
> [out] Pointeur vers une valeur qui indique l’état du contrôle de bouton. L’une des valeurs suivantes peut être renvoyée :
    
MAPI_DISABLED 
  
> Le contrôle de bouton est désactivé et ne peut pas être cliqué. 
    
MAPI_ENABLED 
  
> Le contrôle de bouton est activé et vous pouvez cliquer dessus.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état du contrôle de bouton a été récupéré avec succès.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de services implémentent la méthode **IMAPIControl::GetState** pour fournir à MAPI l’état d’un contrôle de bouton. Si le bouton est activé, il peut répondre à un clic de souris ou à une pression sur la touche. S’il est désactivé, le bouton s’affiche estommité et ne répond pas à un clic de souris ou à une pression sur la touche. 
  
Pour plus d’informations sur l’implémentation de **GetState** et des autres méthodes [IMAPIControl : IUnknown,](imapicontroliunknown.md) voir [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

