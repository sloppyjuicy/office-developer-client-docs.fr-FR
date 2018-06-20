---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Ajoute la personne identifiée par les paramètres emailAddresses et displayName comme un ami pour l’utilisateur connecté sur le réseau social.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787628"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Ajoute la personne identifiée par les paramètres _emailAddresses_ et _displayName_ comme un ami pour l’utilisateur connecté sur le réseau social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Paramètres

_emailAddresses_
  
> [in] Tableau qui contienne une ou plusieurs adresses SMTP valides pour une personne sur le réseau social.
    
_displayName_
  
> [in] Chaîne qui contient le nom complet de la personne à ajouter comme un ami.
    
## <a name="remarks"></a>Remarques

Si le Outlook Social Connector (OSC) fournit plusieurs sur adresse SMTP dans le tableau dans le paramètre **emailAddresses** , le fournisseur OSC pouvez supposer que le premier élément est l’adresse SMTP principale. 
  
Si le fournisseur a la valeur de l’élément **followPerson** comme **true** dans le XML des **fonctionnalités** et aucun des éléments pour _emailAddresses_ correspondent à un utilisateur sur le réseau, le fournisseur doit retourner l’erreur OSC_E_NOT_FOUND. Si le fournisseur a défini **followPerson** comme **false** de **fonctionnalités**, le fournisseur doit renvoyer l’erreur OSC_E_FAIL. 
  
Si la méthode **FollowPersonEx** aboutit, le fournisseur peut utiliser la chaîne dans le paramètre _displayName_ à l’adresse de la personne dans tous les messages envoyés ami-confirmation suivantes, plutôt que d’adressage de la personne à l’adresse SMTP. En revanche, le fournisseur doit être en mesure de gérer l’OSC en passant une chaîne vide pour le paramètre _displayName_ . 
  
Si le fournisseur implémente l’interface [ISocialSession2](isocialsession2iunknown.md) et a défini **followPerson** comme **true** dans le XML des fonctionnalités, l’OSC appelle **FollowPersonEx** au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md). Si le fournisseur a défini **followPerson** **a la valeur True** , mais n’implémente pas l’interface **ISocialSession2** ou **FollowPersonEx** renvoie l’erreur OSC_E_NOTIMPL, l’OSC appelle **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

