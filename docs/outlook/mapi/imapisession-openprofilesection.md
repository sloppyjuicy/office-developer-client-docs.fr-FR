---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439918"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une section du profil actif et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à la section de profil. En passant la valeur NULL, le paramètre _lppProfSect_ renvoie un pointeur vers l'interface standard de la section profil, **IProfSect**.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'accès à la section profil. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement disponible pour le client appelant. Si la section profil n'est pas disponible, un appel ultérieur de celle-ci peut entraîner une erreur. 
    
MAPI_FORCE_ACCESS
  
> Autorise l'accès à une section de profil qui n'appartient pas au fournisseur.
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les sections de profil sont ouvertes avec une autorisation en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. 
    
 _lppProfSect_
  
> remarquer Pointeur vers un pointeur vers la section profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d'accès à une section de profil pour laquelle l'appelant ne dispose pas des autorisations suffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> La section de profil demandée n'existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: OpenProfileSection** ouvre une section de profil ou un objet qui prend en charge l'interface **IProfSect** . Les sections de profil sont utilisées pour lire des informations et écrire des informations dans le profil de session. 
  
Vous ne pouvez pas utiliser **OpenProfileSection** pour ouvrir les sections de profil que les fournisseurs de services individuels possèdent, sauf si vous spécifiez MAPI_FORCE_ACCESS dans le paramètre _ulFlags_ . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Plusieurs clients peuvent ouvrir une section de profil avec une autorisation en lecture seule, mais un seul client peut ouvrir une section de profil avec une autorisation en lecture/écriture. Si un autre client a une section de profil ouverte que vous tentez d'ouvrir en appelant **OpenProfileSection** avec l'indicateur MAPI_MODIFY défini, l'appel échouera, renvoyant MAPI_E_NO_ACCESS. 
  
Une opération d'ouverture en lecture seule échoue si la section est ouverte en écriture. 
  
Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l'indicateur MAPI_MODIFY et une structure **MAPIUID** inexistante dans le paramètre _lpUID_ . Veillez à spécifier MAPI_MODIFY. Si vous définissez _lpUID_ de sorte qu'elle pointe vers un **MAPIUID** inexistant et que **OpenProfileSection** soit configuré pour utiliser le mode d'accès par défaut en lecture seule, l'appel échouera avec MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

