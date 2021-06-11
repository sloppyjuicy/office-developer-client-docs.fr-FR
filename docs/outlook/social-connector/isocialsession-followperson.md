---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Ajoute la personne identifiée par le paramètre emailAddress en tant qu’ami de l’utilisateur connecté sur le réseau social.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423257"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Ajoute la personne identifiée par le  _paramètre emailAddress_ en tant qu’ami de l’utilisateur connecté sur le réseau social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parameters

_emailAddress_
  
> [in] Chaîne qui contient l’adresse e-mail d’une personne.
    
## <a name="remarks"></a>Remarques

Le  _paramètre emailAddress_ doit être une adresse SMTP valide. Si le fournisseur Outlook Social Connector (OSC) a définie  la méthode **followPerson** comme true dans les fonctionnalités **et** que l’argument de _emailAddress_ ne correspond pas à un utilisateur sur le réseau, le fournisseur doit renvoyer l’erreur OSC_E_NOT_FOUND. Si le fournisseur a définie **followPerson** comme **false** dans les **fonctionnalités,** le fournisseur doit renvoyer l’OSC_E_FAIL erreur.
  
Si le fournisseur implémente l’interface [ISocialSession2](isocialsession2iunknown.md) et a définie **followPerson** comme **true** dans les fonctionnalités, l’OSC appelle [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) au lieu de **ISocialSession::FollowPerson**. Si le fournisseur n’implémente pas l’interface **ISocialSession2** ou **si ISocialSession2::FollowPersonEx** renvoie l’erreur OSC_E_NOTIMPL, l’OSC appelle **ISocialSession::FollowPerson** tant que le fournisseur a définie **followPerson** comme **vrai** dans les **fonctionnalités.** Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
Pour décider s’il faut implémenter **ISocalSession::FollowPerson** ou **ISocialSession2::FollowPersonEx,** vous devez déterminer si votre fournisseur a besoin des autres méthodes dans **ISocialSession2** et si vous pouvez utiliser le paramètre  _djsplayName_ dans **FollowPersonEx**.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

