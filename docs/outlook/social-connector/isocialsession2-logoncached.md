---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Ouvre une session sur le site réseau social à l'aide des informations d'identification mises en cache.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436621"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Ouvre une session sur le site réseau social à l'aide des informations d'identification mises en cache.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Paramètres

_connexion_
  
> dans Une chaîne qui peut être vide ou qui contient les informations d'identification de connexion, en fonction du contexte dans lequel OSC appelle **LogonCached**.
    
_userName_
  
> dans Chaîne qui contient le nom d'utilisateur.
    
_mot de passe_
  
> dans Chaîne qui contient le mot de passe de l'utilisateur.
    
_connectOut_
  
> remarquer Chaîne opaque qui contient les informations d'identification.
    
## <a name="remarks"></a>Remarques

Cette méthode est appelée pour l'authentification uniquement si **useLogonCached** est défini sur **true** dans les **fonctionnalités** XML renvoyées par [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md).
  
Outlook Social Connector (OSC) appelle **LogonCached**et transmet une chaîne vide pour les chaînes de _nom d'utilisateur_ et _de mot de passe_ de _connexion_ et non vide. Le fournisseur utilise le _nom d'utilisateur_ et le _mot de passe_ pour se connecter au réseau social et renvoie un paramètre _connectOut_ opaque à OSC si l'authentification réussit. Si l'authentification échoue, le fournisseur renvoie l'erreur OSC_E_LOGON_FAILURE au OSC. 
  
Le paramètre _connectOut_ est une chaîne opaque vers OSC, et est transmis au paramètre _Connect_ sur les tentatives suivantes de l'OSC pour se connecter au réseau social. Le fournisseur doit placer toutes les informations d'identification dans la chaîne _connectOut_ que le fournisseur souhaite que OSC stocke sur les connexions. Le OSC n'interprète pas la chaîne dans _connectOut_et chiffre la chaîne à des fins de sécurité avant de la stocker dans le Registre Windows.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

