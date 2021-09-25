---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Se connecte au site de réseau social à l’aide de l’authentification basée sur les formulaires.
ms.openlocfilehash: 923838f0064d979b7901ebe269822059a75400c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563195"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Se connecte au site de réseau social à l’aide de l’authentification basée sur les formulaires.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Paramètres

_connectIn_
  
> [in] Chaîne **null,** URL d’un formulaire de connexion sur le web ou chaîne qui contient les informations d’identification de connexion, selon le contexte du processus d’connexion lorsque cette méthode est appelée.
    
_connectOut_
  
> [out] Chaîne qui contient les informations d’identification de connexion.
    
## <a name="remarks"></a>Remarques

Le Outlook Social Connector (OSC) appelle la méthode **LogonWeb** uniquement si le fournisseur indique qu’il prend en charge l’authentification basée sur les formulaires. Le fournisseur indique qu’il requiert une authentification basée sur les formulaires en étiquetant **useLogonWebAuth** comme **vrai** dans le XML pour **les fonctionnalités.** Si le fournisseur définit **useLogonWebAuth** comme **false,** l’OSC utilise l’authentification de base et appelle la [méthode ISocialSession::Logon.](isocialsession-logon.md) 
  
La connexion à un site de réseau social à l’aide de l’authentification basée sur les formulaires implique l’appel des méthodes **LogonWeb** et [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) dans un ordre spécifique : 
  
1. L’OSC appelle **LogonWeb** la première fois, en passant la valeur **null** au _paramètre connectIn._ 
    
2. Le fournisseur lève l’erreur OSC_E_AUTH_ERROR à l’OSC.
    
3. L’OSC appelle ensuite **GetLogonUrl**.
    
4. Le fournisseur renvoie l’URL appropriée à une page d’accès dans la **méthode GetLogonUrl.** 
    
5. L’OSC utilise l’URL renvoyée par **GetLogonUrl** pour afficher la page d’inscription basée sur les formulaires. 
    
6. L’OSC appelle ensuite **LogonWeb** une deuxième fois, en passant l’URL au formulaire de connexion dans le _paramètre connectIn._ 
    
7. Si l’authentification réussit, le fournisseur renvoie les informations d’identification de connexion dans le  _paramètre connectOut_ à l’OSC. En cas d’échec de l’authentification, le fournisseur OSC_E_AUTH_ERROR d’erreur à l’OSC. 
    
Si le fournisseur OSC prend en charge la connexion à l’aide des informations d’identification mises en cache, il spécifie **useLogonCached** comme **true** dans le XML **des** fonctionnalités. Le fournisseur doit placer toutes les informations d’identification de connexion dans la chaîne  _connectOut_ que le fournisseur souhaite que l’OSC stocke sur plusieurs connexions. L’OSC n’interprète pas la _chaîne connectOut._ Une fois que l’OSC a vérifié que **l’utilisation deLogonCached** est **vraie,** l’OSC chiffre la chaîne pour des raisons de sécurité avant de la stocker dans Windows registre. L’OSC transmet cette chaîne au paramètre  _connectIn_ lors des tentatives suivantes de connexion au réseau social en appelant [ISocialSession2::LogonCached](isocialsession2-logoncached.md). 
  
Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Authentification basée sur les formulaires](forms-based-authentication.md)

