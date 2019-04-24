---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301546"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une section de profil à partir du profil actuel et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. 
  
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
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique de la section de profil à ouvrir. Les clients ne doivent pas transmettre de valeur NULL pour le paramètre _lpUID_ . Les fournisseurs de services peuvent transmettre la valeur NULL pour récupérer le **MAPIUID** lorsqu'ils appellent à partir de leurs fonctions de point d'entrée de service de messagerie. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à la section de profil. Le passage de la valeur NULL entraîne le renvoi de l'interface standard de la section de profil (**IProfSect**). 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'ouverture de la section profil. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de retourner correctement, éventuellement avant que la section de profil soit entièrement disponible pour l'appelant. Si la section profil n'est pas disponible, un appel ultérieur de celle-ci peut déclencher une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont ouverts en lecture seule, et les appelants ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. Les clients ne sont pas autorisés à accéder en lecture/écriture aux sections du fournisseur du profil.
    
MAPI_FORCE_ACCESS
  
> Autorise l'accès à toutes les sections de profil, même celles appartenant à des fournisseurs de services individuels.
    
 _lppProfSect_
  
> remarquer Pointeur vers un pointeur vers la section profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d'une section de profil en lecture seule ou d'accès à un objet pour lequel l'utilisateur ne dispose pas des autorisations suffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> La section de profil demandée n'existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin:: OpenProfileSection** ouvre une section de profil, permettant ainsi à l'appelant de lire les informations et de les écrire dans le profil actif. 
  
Les clients ne peuvent pas ouvrir les sections de profil qui appartiennent à des fournisseurs à l'aide de la méthode **OpenProfileSection** . 
  
Plusieurs clients ou fournisseurs de services peuvent simultanément ouvrir une section de profil avec une autorisation en lecture seule. Toutefois, lorsqu'une section de profil est ouverte avec une autorisation en lecture/écriture, aucun autre appel ne peut être effectué pour ouvrir la section, quel que soit le type d'accès. Si une section de profil est ouverte avec une autorisation en lecture seule, un appel ultérieur à la demande d'autorisation de lecture/écriture échouera avec MAPI_E_NO_ACCESS. De même, si une section est ouverte avec une autorisation en lecture/écriture, un appel ultérieur à la demande en lecture seule échouera également. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous demandez qu' **OpenProfileSection** ouvre une section de profil inexistante en transmettant MAPI_MODIFY dans _UlFlags_ et un **MAPIUID** inconnu dans _lpUID_, la section de profil est créée. 
  
Si vous demandez à **OpenProfileSection** ouvrir une section inexistante avec l'autorisation en lecture seule, elle renvoie MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la méthode **IProviderAdmin:: OpenProfileSection** pour ouvrir une section de profil à partir du profil actuel.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

