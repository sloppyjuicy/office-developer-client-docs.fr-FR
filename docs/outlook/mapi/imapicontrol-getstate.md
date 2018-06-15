---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783697"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**S’applique à**: Outlook 
  
Récupère une valeur qui indique si le contrôle bouton est activé ou désactivé.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulState_
  
> [out] Pointeur vers une valeur qui indique l’état du contrôle bouton. Une des valeurs suivantes peut être renvoyée :
    
MAPI_DISABLED 
  
> Le contrôle bouton est désactivé et ne peut pas être sélectionné. 
    
MAPI_ENABLED 
  
> Le contrôle bouton est activé et peut être sélectionné.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’état du contrôle bouton a été récupéré correctement.
    
## <a name="remarks"></a>Note

Fournisseurs de services implémentent la méthode **IMAPIControl::GetState** pour fournir MAPI avec l’état d’un contrôle bouton. Si le bouton est activé, il peut répondre à un clic de souris ou la touche. S’il est désactivé, le bouton apparaît en grisé et ne répond pas à un clic de souris ou la touche. 
  
Pour plus d’informations sur la façon d’implémenter **GetState** et l’autre [IMAPIControl : IUnknown](imapicontroliunknown.md) méthodes, voir [Implémentation d’objet de contrôle](control-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

