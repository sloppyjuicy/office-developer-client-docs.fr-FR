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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405659"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une section de profil à partir du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. 
  
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
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique de la section de profil à ouvrir. Les clients ne doivent pas transmettre null pour _le paramètre lpUID._ Les fournisseurs de services peuvent transmettre la valeur NULL pour récupérer **le MAPIUID** lorsqu’ils appellent à partir de leurs fonctions de point d’entrée de service de message. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. La transmission DE NULL entraîne le retour de l’interface standard de la section de profil **(IProfSect).** 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la section de profil est ouverte. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProfileSection** de renvoyer correctement, éventuellement avant que la section de profil ne soit entièrement disponible pour l’appelant. Si la section de profil n’est pas disponible, un appel ultérieur à celui-ci peut occasioner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec une autorisation en lecture seule et les appelants ne doivent pas fonctionner sur l’hypothèse que l’autorisation lecture/écriture a été accordée. Les clients ne sont pas autorisés à lire/écrire des sections fournisseur du profil.
    
MAPI_FORCE_ACCESS
  
> Permet d’accéder à toutes les sections de profil, même celles qui sont propriétés de fournisseurs de services individuels.
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La section profil a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d’une section de profil en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été tentée.
    
MAPI_E_NOT_FOUND 
  
> La section de profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La **méthode IProviderAdmin::OpenProfileSection** ouvre une section de profil, permettant à l’appelant de lire des informations dans le profil actif et éventuellement d’écrire des informations dans celui-ci. 
  
Les clients ne peuvent pas ouvrir les sections de profil appartenant à des fournisseurs à l’aide de la méthode **OpenProfileSection.** 
  
Plusieurs clients ou fournisseurs de services peuvent ouvrir simultanément une section de profil avec une autorisation en lecture seule. Toutefois, lorsqu’une section de profil est ouverte avec une autorisation de lecture/écriture, aucun autre appel ne peut être effectué pour ouvrir la section, quel que soit le type d’accès. Si une section de profil est ouverte avec une autorisation en lecture seule, un appel ultérieur pour demander une autorisation de lecture/écriture échouera avec MAPI_E_NO_ACCESS. De même, si une section est ouverte avec une autorisation de lecture/écriture, un appel ultérieur pour demander une autorisation en lecture seule échouera également. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous demandez **qu’OpenProfileSection** ouvre une section de profil inexistante en passant des MAPI_MODIFY dans  _ulFlags_ et un **MAPIUID** inconnu dans  _lpUID,_ la section de profil est créée. 
  
Si vous demandez **qu’OpenProfileSection** ouvre une section inexistante avec une autorisation en lecture seule, elle renvoie MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la méthode **IProviderAdmin::OpenProfileSection** pour ouvrir une section de profil à partir du profil actuel.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

