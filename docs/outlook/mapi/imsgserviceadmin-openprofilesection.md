---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317392"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
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
  
> Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à la section de profil. Le fait de transmettre NULL génère un pointeur vers son interface standard renvoyée dans le paramètre _lppProfSect_ . L'interface standard d'une section de profil est **IProfSect**.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'accès à la section profil. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement disponible pour le client appelant. Si la section profil n'est pas disponible, un appel ultérieur de celle-ci peut déclencher une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les sections de profil sont ouvertes avec une autorisation en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. 
    
MAPI_FORCE_ACCESS
  
> Autorise l'accès à toutes les sections de profil, même celles appartenant à des fournisseurs de services individuels.
    
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

La méthode **IMsgServiceAdmin:: OpenProfileSection** ouvre une section de profil, un objet qui prend en charge l'interface [IProfSect](iprofsectimapiprop.md) . Les sections de profil sont utilisées pour lire des informations et écrire des informations dans le profil de session. 
  
 **OpenProfileSection** ne peut pas être utilisé pour ouvrir des sections de profil appartenant à des fournisseurs de services individuels, sauf si MAPI_FORCE_ACCESS est utilisé. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Plusieurs clients peuvent ouvrir une section de profil avec une autorisation en lecture seule, mais un seul client peut ouvrir une section de profil avec une autorisation en lecture/écriture. Si un autre client a une section de profil ouverte que vous tentez d'ouvrir en appelant **OpenProfileSection** avec l'indicateur MAPI_MODIFY défini, l'appel échouera, renvoyant MAPI_E_NO_ACCESS. 
  
Une opération d'ouverture en lecture seule échoue si la section est ouverte en écriture. 
  
Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l'indicateur MAPI_MODIFY et une structure [MAPIUID](mapiuid.md) inexistante dans le paramètre _lpUID_ . Veillez à spécifier MAPI_MODIFY. Si vous définissez _lpUID_ de sorte qu'elle pointe vers un **MAPIUID** inexistant et que **OpenProfileSection** soit configuré pour utiliser le mode d'accès par défaut en lecture seule, l'appel échouera avec MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin:: OpenProfileSection** pour ouvrir une section de profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

