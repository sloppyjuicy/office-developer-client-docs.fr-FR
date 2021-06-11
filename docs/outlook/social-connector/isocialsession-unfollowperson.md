---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Supprime la personne identifiée par le paramètre userID en tant qu’ami sur le réseau social.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418434"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Supprime la personne identifiée par le paramètre  _userID_ en tant qu’ami sur le réseau social. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameters

_userID_
  
> [in] Chaîne qui contient un ID d’utilisateur de réseau social pour une personne.
    
## <a name="remarks"></a>Remarques

Le  _paramètre userID_ doit être un ID d’utilisateur valide pour la personne sur le réseau social. 
  
Si le fournisseur Outlook Social Connector (OSC) a définie **doNotFollowPerson** comme **true** dans le XML pour les fonctionnalités, le fournisseur doit renvoyer l’erreur OSC_E_NOT_FOUND dans le cas où l’ID d’utilisateur transmis ne correspond pas à un utilisateur sur le réseau. Si le fournisseur a définie **doNotFollowPerson** comme **false** dans les **fonctionnalités,** le fournisseur doit renvoyer l’OSC_E_FAIL erreur. Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

