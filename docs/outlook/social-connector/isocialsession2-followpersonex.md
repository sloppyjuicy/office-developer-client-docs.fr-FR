---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Ajoute la personne identifiée par les paramètres emailAddresses et displayName en tant qu’ami de l’utilisateur connecté sur le réseau social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429830"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Ajoute la personne identifiée par les paramètres  _emailAddresses_ et  _displayName_ en tant qu’ami de l’utilisateur connecté sur le réseau social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Paramètres

_emailAddresses_
  
> [in] Tableau qui contient une ou plusieurs adresses SMTP valides pour une personne sur le réseau social.
    
_displayName_
  
> [in] Chaîne qui contient le nom complet de la personne à ajouter en tant qu’ami.
    
## <a name="remarks"></a>Remarques

Si Outlook Social Connector (OSC) fournit davantage que l’adresse SMTP dans le tableau dans le paramètre **emailAddresses,** le fournisseur OSC peut supposer que le premier élément est l’adresse SMTP principale. 
  
Si le fournisseur a définie l’élément **followPerson** comme **vrai** dans le **XML** de fonctionnalités et qu’aucun des éléments pour  _emailAddresses_ ne correspond à un utilisateur sur le réseau, le fournisseur doit renvoyer l’erreur OSC_E_NOT_FOUND. Si le fournisseur a définie **followPerson** comme **false** dans les **fonctionnalités,** le fournisseur doit renvoyer l’OSC_E_FAIL erreur. 
  
Si la méthode **FollowPersonEx** réussit, le fournisseur peut utiliser la chaîne dans le paramètre  _displayName_ pour adresser la personne dans n’importe quel e-mail de confirmation d’ami ultérieur, plutôt que de l’adresser à la personne par l’adresse SMTP. En revanche, le fournisseur doit être en mesure de gérer l’OSC en passant une chaîne vide pour le _paramètre displayName._ 
  
Si le fournisseur implémente l’interface [ISocialSession2](isocialsession2iunknown.md) et a définie **followPerson** comme **true** dans le XML de fonctionnalités, l’OSC appelle **FollowPersonEx** au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md). Si le fournisseur a définie **followPerson** comme **true** mais n’implémente pas l’interface **ISocialSession2,** ou **si FollowPersonEx** renvoie l’erreur OSC_E_NOTIMPL, l’OSC appelle **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

