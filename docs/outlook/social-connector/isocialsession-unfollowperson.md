---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Supprime la personne identifiée par le paramètre userID comme un ami sur le réseaux sociaux.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787619"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Supprime la personne identifiée par le paramètre _userID_ comme un ami sur le réseaux sociaux. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Paramètres

_nom d’utilisateur_
  
> [in] Chaîne qui contient un ID d’utilisateur de réseau social d’une personne.
    
## <a name="remarks"></a>Remarques

Le paramètre _userID_ doit être un ID d’utilisateur valide pour la personne sur le réseau social. 
  
Si le fournisseur Outlook Social Connector (OSC) a configuré **doNotFollowPerson** comme **true** dans le code XML des **capacités**, le fournisseur doit retourner l’erreur OSC_E_NOT_FOUND dans ce cas que l’utilisateur QU'ID transmis ne correspond pas à un utilisateur sur le réseau. Si le fournisseur a défini **doNotFollowPerson** comme **false** de **fonctionnalités**, le fournisseur doit renvoyer l’erreur OSC_E_FAIL. Pour plus d’informations sur les codes d’erreur, voir [Codes d’erreur de fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

