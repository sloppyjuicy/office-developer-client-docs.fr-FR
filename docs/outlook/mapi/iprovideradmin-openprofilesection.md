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
ms.openlocfilehash: 276a2bd84156e9b396df71f51130e6704ad7c7fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784407"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**S’applique à**: Outlook 
  
Ouvre une section de profil du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès. 
  
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
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique de la section de profil à ouvrir. Les clients ne doivent pas passer NULL pour le paramètre _lpUID_ . Fournisseurs de services peuvent passer la valeur NULL pour récupérer le **MAPIUID** quand ils appellent à partir de leurs fonctions de point d’entrée de message service. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. Interface standard de la section de profil (**IProfSect**) renvoyé génère passant NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le mode d’ouverture de la section de profil. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenProfileSection** renvoyer avec succès, éventuellement avant la section profil est entièrement disponible à l’appelant. Si la section profil n’est pas disponible, vous appelez suivante pour qu’il peut déclencher une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec l’autorisation en lecture seule, et les appelants ne doivent pas travailler sur l’hypothèse que bénéficie des autorisations en lecture/écriture. Autorisation de lecture/écriture aux sections du fournisseur du profil ne sont pas autorisés par les clients.
    
MAPI_FORCE_ACCESS
  
> Permet d’accéder à toutes les sections de profil, y compris ceux détenus par les fournisseurs de services individuels.
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La section profil a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour modifier une section de profil en lecture seule ou pour accéder à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_FOUND 
  
> La section profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IProviderAdmin::OpenProfileSection** ouvre une section de profil, l’activation de l’appelant et lire des informations d’écrire éventuellement des informations dans le profil actif. 
  
Les clients ne peuvent pas ouvrir les sections profil qui appartiennent à un fournisseur à l’aide de la méthode **OpenProfileSection** . 
  
Plusieurs clients ou fournisseurs de services peuvent ouvrir simultanément une section de profil avec l’autorisation en lecture seule. Toutefois, lorsqu’une section de profil est ouverte avec l’autorisation de lecture/écriture, aucun autre appel ne peut être effectuées pour ouvrir la section, quel que soit le type d’accès. Si une section de profil est ouverte avec l’autorisation en lecture seule, un autre appel à la demande d’autorisation de lecture/écriture échoue avec MAPI_E_NO_ACCESS. De même, si une section est ouverte avec l’autorisation de lecture/écriture, un appel suivant à la demande d’autorisation en lecture seule échouera également. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si vous avez demandé qui **OpenProfileSection** ouvrir une section de profil inexistant en transmettant _n’ulFlags_ et un inconnu **MAPIUID** dans _lpUID_, la section profil sera créée. 
  
Si vous avez demandé que **OpenProfileSection** ouvrir une section inexistante disposant d’une autorisation en lecture seule, elle renvoie MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la méthode **IProviderAdmin::OpenProfileSection** pour ouvrir une section de profil du profil actuel.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

