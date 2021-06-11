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
  
Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. La transmission de null entraîne  _le paramètre lppProfSect_ à renvoyer un pointeur vers l’interface standard de la section de profil, **IProfSect**.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’accès à la section de profil. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de renvoyer correctement, éventuellement avant que la section de profil soit entièrement disponible pour le client appelant. Si la section de profil n’est pas disponible, un appel ultérieur à celui-ci peut provoquer une erreur. 
    
MAPI_FORCE_ACCESS
  
> Permet d’accéder à une section de profil qui n’appartient pas au fournisseur.
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les sections de profil sont ouvertes avec une autorisation en lecture seule et les clients ne doivent pas travailler sur l’hypothèse que l’autorisation lecture/écriture a été accordée. 
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à une section de profil pour laquelle l’appelant dispose d’autorisations insuffisantes a été tentée.
    
MAPI_E_NOT_FOUND 
  
> La section de profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::OpenProfileSection** ouvre une section de profil ou un objet qui prend en charge l’interface **IProfSect.** Les sections de profil sont utilisées pour lire et écrire des informations dans le profil de session. 
  
Vous ne pouvez pas utiliser **OpenProfileSection** pour ouvrir des sections de profil propres à des fournisseurs de services individuels, sauf si vous spécifiez MAPI_FORCE_ACCESS dans le _paramètre ulFlags._ 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Plusieurs clients peuvent ouvrir une section de profil avec une autorisation en lecture seule, mais un seul client peut ouvrir une section de profil avec une autorisation de lecture/écriture. Si une section de profil est ouverte sur un autre client que vous essayez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY, l’appel échoue et retourne MAPI_E_NO_ACCESS. 
  
Une opération d’ouverture en lecture seule échoue si la section est ouverte pour écriture. 
  
Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY et une structure **MAPIUID** inexistante dans le paramètre _lpUID._ Assurez-vous de spécifier MAPI_MODIFY. Si vous définissez _lpUID_ de façon à pointer vers un **MAPIUID** inexistant et qu’OpenProfileSection est définie pour utiliser le mode d’accès par défaut en lecture seule, l’appel échouera avec MAPI_E_NOT_FOUND.  
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

