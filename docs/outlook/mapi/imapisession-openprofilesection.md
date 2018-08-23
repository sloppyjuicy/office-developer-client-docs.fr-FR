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
ms.openlocfilehash: feb12be5cc836a0c7ff90dd5054a34d9df4b6622
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568188"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès. 
  
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
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. Passage de NULL entraîne le paramètre _lppProfSect_ renvoyer un pointeur vers l’interface standard de la section de profil, **IProfSect**.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’accès à la section de profil. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenProfileSection** retournée correctement, éventuellement avant le profil de section est totalement disponible au client appelant. Si la section profil n’est pas disponible, vous appelez suivante lui peut provoquer une erreur. 
    
MAPI_FORCE_ACCESS
  
> Permet d’accéder à une section de profil n’appartenant pas au fournisseur.
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les sections de profil sont ouverts avec l’autorisation en lecture seule et clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture. 
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La section profil a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour accéder à une section de profil pour lequel l’appelant dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_FOUND 
  
> La section profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::OpenProfileSection** ouvre une section de profil ou un objet qui prend en charge l’interface **IProfSect** . Les sections de profil sont utilisées pour la lecture et l’écriture d’informations sur le profil de la session. 
  
Vous ne pouvez pas utiliser **OpenProfileSection** pour ouvrir des sections de profil que propre de fournisseurs de services individuels, sauf si vous spécifiez dans le paramètre _ulFlags_ MAPI_FORCE_ACCESS. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Plusieurs clients peuvent ouvrir une section de profil avec l’autorisation en lecture seule, mais qu’un seul client peut ouvrir une section de profil avec l’autorisation de lecture/écriture. Si un autre client a une section de profil ouvrir que vous essayez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur n’est défini, l’appel échoue, renvoi MAPI_E_NO_ACCESS. 
  
Une opération d’ouverture en lecture seule échoue si la section est ouverte en écriture. 
  
Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur n’et une structure **MAPIUID** qui n’existe pas dans le paramètre _lpUID_ . N’oubliez pas que vous spécifiez ne. Si vous définissez _lpUID_ pour pointer vers un inexistante **MAPIUID** et **OpenProfileSection** est configuré pour utiliser le mode par défaut l’accès en lecture seule, l’appel échoue avec le message MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

