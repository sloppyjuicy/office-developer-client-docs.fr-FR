---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 648170f256763d2ce98bce35ae686aa724db43f0
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464730"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
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

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. Le passage de NULL entraîne le retour d’un pointeur vers son interface standard dans le paramètre _lppProfSect_ . L’interface standard pour une section de profil est **IProfSect**.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’accès à la section de profil. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de renvoyer correctement, éventuellement avant que la section de profil soit entièrement disponible pour le client appelant. Si la section de profil n’est pas disponible, un appel ultérieur à celui-ci peut occasioner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les sections de profil sont ouvertes avec une autorisation en lecture seule et les clients ne doivent pas travailler sur l’hypothèse que l’autorisation lecture/écriture a été accordée. 
    
MAPI_FORCE_ACCESS
  
> Permet d’accéder à toutes les sections de profil, même celles qui sont propriétés de fournisseurs de services individuels.
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section de profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à une section de profil pour laquelle l’appelant dispose d’autorisations insuffisantes a été tentée.
    
MAPI_E_NOT_FOUND 
  
> La section de profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgServiceAdmin::OpenProfileSection** ouvre une section de profil, un objet qui prend en charge l’interface [IProfSect](iprofsectimapiprop.md) . Les sections de profil sont utilisées pour lire et écrire des informations dans le profil de session. 
  
 **OpenProfileSection** ne peut pas être utilisé pour ouvrir des sections de profils propriétés par des fournisseurs de services individuels, sauf si MAPI_FORCE_ACCESS est utilisé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Plusieurs clients peuvent ouvrir une section de profil avec une autorisation en lecture seule, mais un seul client peut ouvrir une section de profil avec une autorisation de lecture/écriture. Si une section de profil est ouverte sur un autre client que vous essayez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY, l’appel échoue et MAPI_E_NO_ACCESS. 
  
Une opération d’ouverture en lecture seule échoue si la section est ouverte pour écriture. 
  
Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY et une structure [MAPIUID](mapiuid.md) inexistante dans le paramètre _lpUID_ . Assurez-vous de spécifier MAPI_MODIFY. Si vous définissez  _lpUID_ de façon à pointer vers un **MAPIUID** inexistant et **qu’OpenProfileSection** est définie pour utiliser le mode d’accès par défaut en lecture seule, l’appel échouera avec MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la **méthode IMsgServiceAdmin::OpenProfileSection** pour ouvrir une section de profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

