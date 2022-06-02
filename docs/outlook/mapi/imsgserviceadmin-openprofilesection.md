---
title: IMsgServiceAdminOpenProfileSection
description: IMsgServiceAdmin OpenProfileSection ouvre une section du profil actuel et retourne un pointeur IProfSect pour un accès supplémentaire.
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
ms.openlocfilehash: 0a37865188c2aca6901908826efb03b363d9ffc5
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828559"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. 
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. Le passage de NULL entraîne le retour d’un pointeur vers son interface standard dans le paramètre _lppProfSect_ . L’interface standard d’une section de profil est **IProfSect**.
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle l’accès à la section de profil. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement disponible pour le client appelant. Si la section de profil n’est pas disponible, un appel ultérieur à celle-ci peut générer une erreur. 
    
MAPI_MODIFY 
  
> Demande l’autorisation de lecture/écriture. Par défaut, les sections de profil sont ouvertes avec une autorisation en lecture seule, et les clients ne doivent pas travailler sur l’hypothèse que l’autorisation de lecture/écriture a été accordée. 
    
MAPI_FORCE_ACCESS
  
> Autorise l’accès à toutes les sections de profil, même celles appartenant à des fournisseurs de services individuels.
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section de profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à une section de profil pour laquelle l’appelant dispose d’autorisations insuffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> La section de profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::OpenProfileSection** ouvre une section de profil, un objet qui prend en charge l’interface [IProfSect](iprofsectimapiprop.md) . Les sections de profil sont utilisées pour lire des informations et écrire des informations dans le profil de session. 
  
 **OpenProfileSection** ne peut pas être utilisé pour ouvrir des sections de profil appartenant à des fournisseurs de services individuels, sauf si MAPI_FORCE_ACCESS est utilisé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Plusieurs clients peuvent ouvrir une section de profil avec une autorisation en lecture seule, mais un seul client peut ouvrir une section de profil avec une autorisation de lecture/écriture. Si un autre client a une section de profil ouverte que vous tentez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY défini, l’appel échoue, renvoyant MAPI_E_NO_ACCESS. 
  
Une opération d’ouverture en lecture seule échoue si la section est ouverte pour l’écriture. 
  
Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur MAPI_MODIFY et une structure [MAPIUID](mapiuid.md) inexistante dans le paramètre _lpUID_ . Veillez à spécifier MAPI_MODIFY. Si vous définissez  _lpUID_ pour qu’il pointe vers un **MAPIUID** inexistant et **qu’OpenProfileSection** utilise le mode d’accès par défaut en lecture seule, l’appel échoue avec MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::OpenProfileSection** pour ouvrir une section de profil. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

