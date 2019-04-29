---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Récupère une interface ISocialSession configurée automatiquement.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417440"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement. 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Paramètres

_session_
  
> [out] Une interface **ISocialSession**. 
    
## <a name="remarks"></a>Remarques

L’interface **ISocialSession** renvoyée est automatiquement connectée au réseau, selon une méthode propre au fournisseur. 
  
Le fournisseur doit renvoyer l’erreur OSC_E_NOT_IMPLEMENTED si le réseau social ne prend pas en charge la configuration automatique. Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

