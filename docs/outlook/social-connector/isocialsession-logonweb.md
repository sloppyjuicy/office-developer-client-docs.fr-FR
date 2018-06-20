---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Ouvre une session sur le site de réseau social à l’aide de l’authentification basée sur les formulaires.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787618"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Ouvre une session sur le site de réseau social à l’aide de l’authentification basée sur les formulaires.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Paramètres

_connectIn_
  
> [in] Chaîne qui est **null**, une URL à un formulaire d’ouverture de session sur le site web ou une chaîne qui contient les informations d’identification d’ouverture de session, selon le contexte du processus d’ouverture de session lorsque cette méthode est appelée.
    
_connectOut_
  
> [out] Chaîne qui contient les informations d’identification d’ouverture de session.
    
## <a name="remarks"></a>Remarques

L’Outlook Social Connector (OSC) appelle la méthode **LogonWeb** uniquement si le fournisseur indique qu’il prend en charge l’authentification basée sur les formulaires. Le fournisseur indique qu’il exige l’authentification basée sur les formulaires en définissant **useLogonWebAuth** comme **true** dans le code XML des **capacités**. Si le fournisseur définit **useLogonWebAuth** comme **false**, l’OSC utilise l’authentification de base et appelle la méthode [ISocialSession::Logon](isocialsession-logon.md) . 
  
Se connecter à un site de réseau social à l’aide de l’authentification basée sur les formulaires implique d’appeler les méthodes **LogonWeb** et [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) dans un ordre spécifique : 
  
1. L’OSC appelle **LogonWeb** la première fois, en passant **null** au paramètre _connectIn_ . 
    
2. Le fournisseur génère l’erreur OSC_E_AUTH_ERROR à l’OSC.
    
3. L’OSC appelle ensuite **GetLogonUrl**.
    
4. Le fournisseur renvoie l’URL appropriée à une page d’ouverture de session dans la méthode **GetLogonUrl** . 
    
5. L’OSC utilise l’URL renvoyée par **GetLogonUrl** pour afficher la page d’ouverture de session basée sur les formulaires. 
    
6. L’OSC appelle ensuite **LogonWeb** une deuxième fois, en transmettant l’URL du formulaire d’ouverture de session dans le paramètre _connectIn_ . 
    
7. Si l’authentification réussit, le fournisseur retourne les informations d’identification d’ouverture de session dans le paramètre _connectOut_ à l’OSC. Si l’authentification échoue, le fournisseur déclenche l’erreur OSC_E_AUTH_ERROR à l’OSC. 
    
Si le fournisseur OSC prend en charge la connexion à l’aide des informations d’identification mises en cache, il spécifie **useLogonCached** comme **true** dans le XML des **fonctionnalités** . Le fournisseur doit placer les informations d’identification d’ouverture de session dans la chaîne _connectOut_ que le fournisseur souhaite l’OSC pour stocker les connexions. L’OSC n’interprète pas la chaîne _connectOut_ . Une fois l’OSC vérifie **useLogonCached** a la **valeur true**, l’OSC chiffre la chaîne pour la sécurité avant de les stocker dans le Registre Windows. L’OSC transmet cette chaîne au paramètre _connectIn_ lors des tentatives suivantes pour vous connecter au réseau social en appelant [ISocialSession2::LogonCached](isocialsession2-logoncached.md). 
  
Pour plus d’informations sur les codes d’erreur, voir [Codes d’erreur de fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Authentification basée sur les formulaires](forms-based-authentication.md)

