---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Se connecte au site de réseau social à l’aide des informations d’identification mises en cache.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436621"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Se connecte au site de réseau social à l’aide des informations d’identification mises en cache.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameters

_connectIn_
  
> [in] Chaîne qui peut être vide ou qui contient les informations d’identification de connexion, selon le contexte dans lequel OSC appelle **LogonCached**.
    
_userName_
  
> [in] Chaîne qui contient le nom d’utilisateur.
    
_mot de passe_
  
> [in] Chaîne qui contient le mot de passe de l’utilisateur.
    
_connectOut_
  
> [out] Chaîne opaque qui contient des informations d’identification.
    
## <a name="remarks"></a>Remarques

Cette méthode est appelée pour l’authentification uniquement si **useLogonCached** est définie comme **true** dans les fonctionnalités **XML** renvoyées par [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).
  
Le Outlook Social Connector (OSC) appelle **LogonCached** et transmet une chaîne vide pour les chaînes _connectIn_ et _userName_ et _password_ non vides. Le fournisseur utilise _userName_ et le mot de passe pour se connecter au réseau social et renvoie un paramètre _opaque connectOut_ à l’OSC si l’authentification réussit.  En cas d’échec de l’authentification, le fournisseur renvoie OSC_E_LOGON_FAILURE erreur de message à l’OSC. 
  
Le  _paramètre connectOut_ est une chaîne opaque à OSC et est transmis au paramètre  _connectIn_ lors des tentatives ultérieures de connexion au réseau social par l’OSC. Le fournisseur doit placer toutes les informations d’identification dans la  _chaîne connectOut_ que le fournisseur souhaite que l’OSC stocke sur plusieurs connexions. L’OSC n’interprète pas la chaîne dans _connectOut_ et chiffre la chaîne à des fins de sécurité avant de la stocker dans Windows registre.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

