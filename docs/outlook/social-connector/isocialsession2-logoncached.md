---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Ouvre une session sur le site de réseau social à l’aide des informations d’identification mises en cache.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787625"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Ouvre une session sur le site de réseau social à l’aide des informations d’identification mises en cache.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Paramètres

_connectIn_
  
> [in] Chaîne qui peut être vide ou contient les informations d’identification d’ouverture de session, selon le contexte dans lequel l’OSC appelle **LogonCached**.
    
_userName_
  
> [in] Chaîne qui contient le nom d’utilisateur.
    
_mot de passe_
  
> [in] Chaîne qui contient le mot de passe.
    
_connectOut_
  
> [out] Une chaîne opaque qui contient les informations d’identification.
    
## <a name="remarks"></a>Remarques

Cette méthode est appelée pour l’authentification uniquement si **useLogonCached** est définie comme **true** dans le XML des **fonctionnalités** renvoyé par [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).
  
L’Outlook Social Connector (OSC) appelle **LogonCached**et transmet une chaîne vide pour _connectIn_ et chaînes de _nom d’utilisateur_ et _mot de passe_ non vide. Le fournisseur utilise le _nom d’utilisateur_ et _mot de passe_ pour vous connecter au réseau social et retourne un paramètre opaque _connectOut_ à l’OSC si l’authentification réussit. Si l’authentification échoue, le fournisseur renvoie l’erreur OSC_E_LOGON_FAILURE à l’OSC. 
  
Le paramètre _connectOut_ est une chaîne opaque à l’OSC et est transmis au paramètre _connectIn_ lors des tentatives suivantes à l’OSC à se connecter au réseau social. Le fournisseur doit placer les informations d’identification dans la chaîne _connectOut_ que le fournisseur souhaite l’OSC pour stocker les connexions. L’OSC n’interprète pas la chaîne de _connectOut_et chiffre la chaîne pour des raisons de sécurité avant de les stocker dans le Registre Windows.
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

