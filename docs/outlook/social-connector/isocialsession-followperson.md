---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Ajoute la personne identifiée par le paramètre emailAddress en tant qu'ami pour l'utilisateur connecté sur le réseau social.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285363"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Ajoute la personne identifiée par le paramètre _EmailAddress_ en tant qu'ami pour l'utilisateur connecté sur le réseau social. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Paramètres

_emailAddress_
  
> dans Chaîne qui contient l'adresse de messagerie d'une personne.
    
## <a name="remarks"></a>Remarques

Le paramètre _EmailAddress_ doit être une adresse SMTP valide. Si le fournisseur Outlook Social Connector (OSC) a défini la méthode **followPerson** comme **true** dans les **fonctionnalités**et que l'argument de _EmailAddress_ ne correspond pas à un utilisateur sur le réseau, le fournisseur doit renvoyer l'OSC_E_NOT_FOUND «. Si le fournisseur a défini **followPerson** comme **false** dans les **fonctionnalités**, le fournisseur doit renvoyer l'erreur OSC_E_FAIL.
  
Si le fournisseur implémente l'interface [ISocialSession2](isocialsession2iunknown.md) et a défini **followPerson** en tant que **true** dans les **fonctionnalités**, OSC appelle [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) au lieu de **ISocialSession:: followPerson **. Si le fournisseur n'implémente pas l'interface **ISocialSession2** , ou **ISocialSession2:: FollowPersonEx** renvoie l'erreur OSC_E_NOTIMPL, le OSC appelle **ISocialSession:: followPerson** tant que le fournisseur a défini ** followPerson** comme **true** dans les **fonctionnalités**. Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
Lorsque vous décidez s'il faut implémenter **ISocalSession:: followPerson** ou **ISocialSession2:: FollowPersonEx**, vous devez déterminer si votre fournisseur a besoin des autres méthodes dans **ISocialSession2**et si vous pouvez utiliser le _ paramètre djsplayName_ dans **FollowPersonEx**.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

