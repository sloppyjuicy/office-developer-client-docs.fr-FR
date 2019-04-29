---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Ouvre une session sur le site réseau social à l'aide de l'authentification basée sur les formulaires.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430335"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Ouvre une session sur le site réseau social à l'aide de l'authentification basée sur les formulaires.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Paramètres

_connexion_
  
> dans Une chaîne qui est **null**, une URL vers un formulaire de connexion sur le Web ou une chaîne qui contient les informations d'identification de connexion, en fonction du contexte dans le processus d'ouverture de session lors de l'appel de cette méthode.
    
_connectOut_
  
> remarquer Chaîne qui contient les informations d'identification d'ouverture de session.
    
## <a name="remarks"></a>Remarques

Outlook Social Connector (OSC) appelle la méthode **LogonWeb** uniquement si le fournisseur indique qu'il prend en charge l'authentification basée sur les formulaires. Le fournisseur indique qu'il nécessite l'authentification basée sur les formulaires en définissant **useLogonWebAuth** comme **true** dans le code XML pour les **fonctionnalités**. Si le fournisseur définit **useLogonWebAuth** comme **false**, le OSC utilise l'authentification de base et appelle la méthode [ISocialSession:: Logon](isocialsession-logon.md) . 
  
La connexion à un site de réseau social à l'aide de l'authentification basée sur les formulaires implique l'appel des méthodes **LogonWeb** et [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) dans un ordre spécifique: 
  
1. Le OSC appelle **LogonWeb** la première fois, en transmettant la **valeur null** au paramètre _Connect_ . 
    
2. Le fournisseur déclenche l'erreur OSC_E_AUTH_ERROR au OSC.
    
3. Le OSC appelle ensuite **GetLogonUrl**.
    
4. Le fournisseur renvoie l'URL appropriée à une page de connexion dans la méthode **GetLogonUrl** . 
    
5. Le OSC utilise l'URL renvoyée par **GetLogonUrl** pour afficher la page d'ouverture de session basée sur des formulaires. 
    
6. Le OSC appelle ensuite **LogonWeb** une deuxième fois, en transmettant l'URL au formulaire d'ouverture de session dans le paramètre _Connect_ . 
    
7. Si l'authentification réussit, le fournisseur renvoie les informations d'identification d'ouverture de session dans le paramètre _connectOut_ dans le OSC. Si l'authentification échoue, le fournisseur déclenche l'erreur OSC_E_AUTH_ERROR au OSC. 
    
Si le fournisseur OSC prend en charge l'ouverture de session à l'aide des informations d'identification mises en cache, il spécifie **useLogonCached** comme **true** dans les **fonctionnalités** XML. Le fournisseur doit placer toutes les informations d'identification d'ouverture de session dans la chaîne _connectOut_ que le fournisseur veut que OSC stocke sur les connexions. Le OSC n'interprète pas la chaîne _connectOut_ . Une fois que le contrôle OSC a vérifié que **useLogonCached** a la **valeur true**, le contrôle OSC chiffre la chaîne à des fins de sécurité avant de la stocker dans le Registre Windows. L'OSC transmet cette chaîne au paramètre _Connect_ lors des tentatives suivantes de connexion au réseau social en appelant [ISocialSession2:: LogonCached](isocialsession2-logoncached.md). 
  
Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Authentification basée sur les formulaires](forms-based-authentication.md)

