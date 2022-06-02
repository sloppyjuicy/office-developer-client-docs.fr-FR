---
title: IProviderAdminOpenProfileSection
description: IProviderAdmin OpenProfileSection ouvre une section de profil à partir du profil actuel et retourne un pointeur IProfSect pour un accès supplémentaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
ms.openlocfilehash: 1a59db51ca9b00196ddd18870ea54da4edcdcd75
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65826945"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une section de profil à partir du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. 
  
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
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique de la section de profil à ouvrir. Les clients ne doivent pas passer null pour le paramètre  _lpUID_ . Les fournisseurs de services peuvent passer null pour récupérer le **MAPIUID** lorsqu’ils appellent à partir de leurs fonctions de point d’entrée de service de message. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. Le passage de la valeur NULL entraîne le retour de l’interface standard (**IProfSect**) de la section de profil. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont la section de profil est ouverte. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement disponible pour l’appelant. Si la section de profil n’est pas disponible, un appel ultérieur à celle-ci peut générer une erreur. 
    
MAPI_MODIFY 
  
> Demande l’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec une autorisation en lecture seule et les appelants ne doivent pas fonctionner en partant du principe que l’autorisation de lecture/écriture a été accordée. Les clients ne sont pas autorisés à accéder en lecture/écriture aux sections fournisseur du profil.
    
MAPI_FORCE_ACCESS
  
> Autorise l’accès à toutes les sections de profil, même celles appartenant à des fournisseurs de services individuels.
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section de profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d’une section de profil en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> La section de profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin::OpenProfileSection** ouvre une section de profil, ce qui permet à l’appelant de lire des informations à partir du profil actif et éventuellement d’écrire des informations dans celui-ci. 
  
Les clients ne peuvent pas ouvrir les sections de profil qui appartiennent à des fournisseurs à l’aide de la méthode **OpenProfileSection** . 
  
Plusieurs clients ou fournisseurs de services peuvent ouvrir simultanément une section de profil avec une autorisation en lecture seule. Toutefois, lorsqu’une section de profil est ouverte avec l’autorisation de lecture/écriture, aucun autre appel ne peut être effectué pour ouvrir la section, quel que soit le type d’accès. Si une section de profil est ouverte avec une autorisation en lecture seule, un appel ultérieur pour demander l’autorisation de lecture/écriture échoue avec MAPI_E_NO_ACCESS. De même, si une section est ouverte avec une autorisation de lecture/écriture, un appel ultérieur pour demander l’autorisation en lecture seule échoue également. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous demandez à **OpenProfileSection** d’ouvrir une section de profil inexistante en passant MAPI_MODIFY dans  _ulFlags_ et un **MAPIUID** inconnu dans  _lpUID_, la section de profil est créée. 
  
Si vous demandez à **OpenProfileSection** d’ouvrir une section inexistante avec une autorisation en lecture seule, elle retourne MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la méthode **IProviderAdmin::OpenProfileSection** pour ouvrir une section de profil à partir du profil actuel. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

