---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Ajoute la personne identifiée par les paramètres emailAddresses et displayName comme un ami pour l'utilisateur connecté sur le réseau social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429830"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Ajoute la personne identifiée par les paramètres _EmailAddresses_ et _DisplayName_ comme un ami pour l'utilisateur connecté sur le réseau social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Paramètres

_emailAddresses_
  
> dans Tableau qui contient une ou plusieurs adresses SMTP valides pour une personne sur le réseau social.
    
_displayName_
  
> dans Chaîne qui contient le nom complet de la personne à ajouter en tant qu'ami.
    
## <a name="remarks"></a>Remarques

Si Outlook Social Connector (OSC) fournit plus de sur l'adresse SMTP dans le tableau dans le paramètre **EmailAddresses** , le fournisseur OSC peut supposer que le premier élément est l'adresse SMTP principale. 
  
Si le fournisseur a défini l'élément **followPerson** comme **true** dans les **fonctionnalités** XML et qu'aucun des éléments de _EmailAddresses_ ne correspond à un utilisateur sur le réseau, le fournisseur doit renvoyer l'erreur OSC_E_NOT_FOUND. Si le fournisseur a défini **followPerson** comme **false** dans les **fonctionnalités**, le fournisseur doit renvoyer l'erreur OSC_E_FAIL. 
  
Si la méthode **FollowPersonEx** réussit, le fournisseur peut utiliser la chaîne dans le paramètre _DisplayName_ pour adresser la personne dans tout message électronique de confirmation Friend suivant, au lieu de l'adresser par l'adresse SMTP. En revanche, le fournisseur doit être en mesure de gérer le OSC en passant une chaîne vide pour le paramètre _DisplayName_ . 
  
Si le fournisseur implémente l'interface [ISocialSession2](isocialsession2iunknown.md) et a défini **followPerson** sur **true** dans les fonctionnalités XML, l'interface OSC appelle **FollowPersonEx** au lieu de [ISocialSession:: followPerson](isocialsession-followperson.md). Si le fournisseur a défini **followPerson** comme **true** mais n'implémente pas l'interface **ISocialSession2** , ou **FollowPersonEx** renvoie l'erreur OSC_E_NOTIMPL, l'interface OSC appelle **ISocialSession:: followPerson**.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

