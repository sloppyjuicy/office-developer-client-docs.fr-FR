---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Obtient une interface ISocialSession configurée automatiquement.
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787620"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Obtient une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement. 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Paramètres

_session_
  
> [out] Une interface **ISocialSession** . 
    
## <a name="remarks"></a>Remarques

L’interface **ISocialSession** retournée est automatiquement connecté au réseau, basé sur une méthode spécifique au fournisseur. 
  
Le fournisseur doit renvoyer l’erreur OSC_E_NOT_IMPLEMENTED si le réseau social ne prend pas en charge la configuration automatique. Pour plus d’informations sur les codes d’erreur, voir [Codes d’erreur de fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

