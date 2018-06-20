---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Ajoute la personne identifiée par le paramètre emailAddress comme un ami pour l’utilisateur connecté sur le réseau social.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787610"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Ajoute la personne identifiée par le paramètre _emailAddress_ comme un ami pour l’utilisateur connecté sur le réseau social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Paramètres

_emailAddress_
  
> [in] Chaîne qui contient une adresse de messagerie d’une personne.
    
## <a name="remarks"></a>Remarques

Le paramètre _emailAddress_ doit être une adresse SMTP valide. Si le fournisseur Outlook Social Connector (OSC) a défini la méthode **followPerson** comme **true** dans les **fonctionnalités**et l’argument pour _emailAddress_ ne correspond pas à un utilisateur sur le réseau, le fournisseur doit retourner la OSC_E_NOT_FOUND erreur. Si le fournisseur a défini **followPerson** comme **false** de **fonctionnalités**, le fournisseur doit renvoyer l’erreur OSC_E_FAIL.
  
Si le fournisseur implémente l’interface [ISocialSession2](isocialsession2iunknown.md) et a défini **followPerson** comme **true** dans les **fonctionnalités**, l’OSC appellera [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) au lieu de **ISocialSession::FollowPerson **. Si le fournisseur n’implémente pas l’interface **ISocialSession2** ou **ISocialSession2::FollowPersonEx** renvoie l’erreur OSC_E_NOTIMPL, l’OSC appellera **ISocialSession::FollowPerson** tant que le fournisseur a la valeur ** followPerson** comme **true** dans les **fonctionnalités**. Pour plus d’informations sur les codes d’erreur, voir [Codes d’erreur de fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
Pour décider si à implémenter **ISocalSession::FollowPerson** ou **ISocialSession2::FollowPersonEx**, vous devez tenir compte si votre fournisseur doit les autres méthodes de **ISocialSession2**et si vous pouvez utiliser la _ djsplayName_ paramètre dans **FollowPersonEx**.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

